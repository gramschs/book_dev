---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.14.7
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# 11.3 Entscheidungsbäume in der Praxis

TODO


## Lernziele

TODO


## Entscheidungsbäume haben Probleme mit Overfitting

Entscheidungsbäume haben viele Vorteile. Ein sehr wichtiger Vorteil ist, dass
sich der fertig trainierte Entscheidungsbaum visualisieren lässt und so leicht
nachvollziehbar wird, welche Eigenschaften einflussreich sind. Ein zweiter
Vorteil ist, dass Entscheidungsbäume auch sehr gut funktionieren, wenn die Daten
sehr unterschiedlich sind. Beispielsweise können numerische und kategoriale
Eigenschaften gleichermaßen als Eingabe dienen. Darüber hinaus können die
numerischen Werte auch auf sehr unterschiedlichen Skalen vorliegen.
Entscheidungsbäume sind bezogen auf die Daten sehr robust und brauchen nur wenig
Datenvorverarbeitung. 

Ein großer Nachteil von Entscheidungsbäumen ist, dass sie eine Tendenz zum
sogenannten **Overfitting** haben. Overfitting könnte man auf deutsch als
**Überanpassung** übersetzen. Wie so oft beim maschinellen Lernen ist der
deutsche Begriff ungebräuchlich, so dass auch wir hier den englischen Begriff
Overfitting und das Gegenteil davon, das sogenannte **Underfitting**
(Unteranpassung) benutzen.

Was ist Overfitting? Betrachten wir erneut das Autohaus-Beispiel, aber diesmal
mit mehr Autos. Wir lassen die Autos diesmal mit einer in Scikit-Learn
eingebauten Funktion zur Generierung von künstlichen Daten erzeugen, der
sogenannten `make_moons`-Funktion (siehe [Dokumentation Scikit-Learn →
make_moons](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_moons.html)) aus dem Module `sklearn.datasets`.

```{code-cell}
from sklearn.datasets import make_moons 

X_array, y_array = make_moons(noise = 0.5, n_samples=50, random_state=3)
```

Damit die künstlichen Daten besser zu dem Autohaus-Beispiel passen,
transformieren wir die Daten folgendermaßen und packen Sie geeignet in
Pandas-Datenstrukturen.

```{code-cell}
import numpy as np
import pandas as pd

# shift all feature values to a positive range and 
# convert it to an integer matrix
X_array = X_array + 1.2 * np.abs(np.min(X_array))
X_array[:,0] = np.ceil(X_array[:,0] * 30000)
X_array[:,1] = np.ceil(X_array[:,1] * 10000)
X = pd.DataFrame(X_array, columns=['Kilometerstand [km]', 'Preis [EUR]'], dtype=(int, int))

# map 0.0 to True and 1.0 to False
y_array = (y_array - 1.0) * (-1)
y = pd.Series(y_array, name='verkauft', dtype='bool')
```

Als nächstes visualisieren wir die Daten.

```{code-cell}
import plotly.express as px

fig = px.scatter(x = X['Kilometerstand [km]'], y = X['Preis [EUR]'], color=y,
    title='Künstliche Daten Autohaus',
    labels={'x': 'Kilometerstand [km]', 'y': 'Preis [EUR]', 'color': 'verkauft'})
fig.show()
```

Das Training des Entscheidungsbaumes und dessen Visualisierung erledigt der
folgende Code.

```{code-cell}
from sklearn.tree import DecisionTreeClassifier, plot_tree

modell = DecisionTreeClassifier(random_state=0)
modell.fit(X,y)

plot_tree(modell,
    feature_names=['Kilometerstand [km]', 'Preis [EUR]'],
    class_names=['nicht verkauft', 'verkauft']);
```

Die Visualisierung des Entscheidungsbaumes zeigt sehr viele Verzweigungen und
die Beschriftung ist kaum noch zu lesen. Der folgende Code visualisiert die
Entscheidungsgrenzen. Leider ist die Visualisierungsmethode von Scikit-Learn
nicht an Plotly, sondern an die alternative »Matplotlib« angepasst, so dass die
Syntax etwas ungewohnt wirkt.

```{code-cell}
import matplotlib.pyplot as plt
import matplotlib as mpl
from matplotlib.colors import ListedColormap
from sklearn.inspection import DecisionBoundaryDisplay

fig = DecisionBoundaryDisplay.from_estimator(modell, X, cmap=ListedColormap(['#EF553B33', '#636EFA33']), grid_resolution=1000)
fig.ax_.scatter(X['Kilometerstand [km]'], X['Preis [EUR]'], c=y, cmap=ListedColormap(['#EF553B', '#636EFA']))
fig.ax_.set_title('Entscheidungsgrenzen');
```

Es ist fraglich, ob dieser Entscheidungsbaum nicht zu genau an die
Trainingsdaten angepasst wurde. Der dünne blaue vertikale Streifen bei ungefähr
97000 km ist wahrscheinlich keine sinnvolle Entscheidung, sondern eher einem
Ausreißer geschuldet (dem Auto mit einem Kilometerstand von 97098 km und einem
Preis von 28229 EUR). Der Entscheidungsbaum hat sich zu stark an die Daten
angepasst. Es ist wahrscheinlich, dass dieser Entscheidungsbaum für Autos mit
einem Kilometerstand von ungefähr 97000 km falsche Prognosen treffen wird. Wenn
wir mit den gleichen Daten erneut einen Entscheidungsbaum trainieren lassen und
den Zufallszahlengenerator mit dem Zustand `random_state=1` initialisieren,
erhalten wir auch ein völlig anderes Ergebnis.

```{code-cell}
modell_alternative = DecisionTreeClassifier(random_state=1)
modell_alternative.fit(X,y)

fig = DecisionBoundaryDisplay.from_estimator(modell_alternative, X, cmap=ListedColormap(['#EF553B33', '#636EFA33']), grid_resolution=1000)
fig.ax_.scatter(X['Kilometerstand [km]'], X['Preis [EUR]'], c=y, cmap=ListedColormap(['#EF553B', '#636EFA']))
fig.ax_.set_title('Entscheidungsgrenzen des alternativen Modells');
```

Eine Möglichkeit, die Überanpassung (Overfitting) an die Daten zu bekämpfen, ist
das Zurechtschneiden (Pruning) der Entscheidungsbäume. Eine andere ist, aus
mehreren Entscheidungbäumen einen »durchschnittlichen« Entscheidungsbaum zu
bilden. Dieses Verfahren heißt Zufallswald (Random Forest) und wird ausführlich
in einem eigenen Kapitel behandelt werden. In diesem Kapitel betrachten wir nur
das Zurechtschneiden der Entscheidungsbäume. 

## Zurechtschneiden von Entscheidungsbäumen

TODO


## Entscheidungsbäume für Regressionsprobleme

TODO


## Zusammenfassung und Ausblick

TODO