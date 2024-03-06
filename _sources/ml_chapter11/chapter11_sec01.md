---
jupytext:
  formats: ipynb,md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.15.2
kernelspec:
  display_name: python39
  language: python
  name: python3
---

# 11.1 Was ist ein Entscheidungsbaum?

TEST

<div id="fig11A">
  <img src="pics/combined_decisiontree00.svg" alt="" />
  <img src="pics/combined_decisiontree02.svg" alt="" />
</div>
<script type="text/javascript">
  const element = document.getElementById("fig11A");
  const viewer = new ImageCompare(element).mount();
</script>


TEST


Ein beliebtes Partyspiel ist das Spiel "Wer bin ich?". Die Spielregel sind
simpel. Eine Person wählt eine berühmte Person oder eine Figur aus einem Film
oder Buch, die die Mitspieler:innen erraten müssen. Die Mitspieler:innen
dürfen jedoch nur Fragen stellen, die mit "Ja" oder "Nein" beantwortet werden. 

Hier ist ein Beispiel, wie eine typische Runde von "Wer bin ich?" ablaufen
könnte:

* Spieler 1: Bin ich männlich?
* Spieler 2: Ja.
* Spieler 3: Bist du ein Schauspieler?
* Spieler 1: Nein.
* Spieler 4: Bist du ein Musiker?
* Spieler 1: Ja.
* Spieler 5: Bist du Michael Jackson?
* Spieler 1: Ja! Richtig!

Als nächstes wäre jetzt Spieler 5 an der Reihe, sich eine Person oder Figur
auszuwählen, die die anderen Spieler erraten sollen. Vielleicht kennen Sie auch
die umgekehrte Variante. Der Name der zu ratenden Person/Figur wird der Person
mit einem Zettel auf die Stirn geklebt. Und nun muss die Person raten, während
die Mitspieler:innen mit Ja/Nein antworten.

Dieser Partyklassiker lässt sich auch auf das maschinelle Lernen übertragen. 


## Lernziele

```{admonition} Lernziele
:class: admonition-goals
* TODO
```


## Ein Entscheidungsbaum im Autohaus

Ein **Entscheidungsbaum** gehört zu den überwachten Lernverfahren. Es ist auch
üblich, die englische Bezeichnung **Decision Tree** anstatt des deutschen
Begriffes zu nutzen. Ein großer Vorteil von Entscheidungsbäumen ist ihre
Flexibilität, denn sie können sowohl für Klassifikations- als auch
Regressionsaufgaben eingesetzt werden. Im Folgenden betrachten wir als Beispiel
eine Klassifikationsaufgabe. In einem Autohaus vereinbaren zehn Personen eine
Probefahrt. In der folgenden Tabelle ist notiert, welchen 

* `Kilometerstand [in km]` und
* `Preis [in EUR]`

das jeweilige Auto hat. In der dritten Spalte `verkauft` ist vermerkt, ob das
Auto nach der Probefahrt verkauft wurde (`True`) oder nicht (`False`). Diese
Information ist die Zielgröße. Die Tabelle mit den Daten lässt sich effizient
mit einem Pandas-DataFrame organisieren:

```{code-cell}
import pandas as pd 

daten = pd.DataFrame({
    'Kilometerstand [km]': [32908, 20328, 13285, 17162, 27449, 13715, 32889,  3111, 15607, 18295],
    'Preis [EUR]': [15960, 20495, 17227, 17851, 5428, 22772, 13581, 16793, 23253, 11382],
    'verkauft': [False, True, False, True, False, True, False, True, True, False],
    },
    index=['Auto 1', 'Auto 2', 'Auto 3', 'Auto 4', 'Auto 5', 'Auto 6', 'Auto 7', 'Auto 8', 'Auto 9', 'Auto 10'])
daten.head(10)
```

Da in unserem Beispiel von den Autos nur die beiden Eigenschaften
`Kilometerstand [km]` und `Preis [EUR]` erfasst wurden, können wir die
Datenpunkte anschaulich in einem zweidimensionalen Streudiagramm (Scatterplot)
visualisieren. Dabei wird der Kilometerstand auf der x-Achse und der Preis auf
der y-Achse abgetragen. Die Zielgröße `verkauft` kennzeichnen wir durch die
Farbe. Dabei steht die Farbe Rot für »verkauft« (True) und Blau für »nicht
verkauft« (False).

```{code-cell}
import plotly.express as px

fig = px.scatter(daten, x = 'Kilometerstand [km]', y = 'Preis [EUR]', 
                 color='verkauft', title='Künstliche Daten: Verkaufsaktion im Autohaus')
fig.show()
```

Als nächstes zeigen wir, wie die Autos anhand von Fragen in die beiden Klassen
»verkauft« und »nicht verkauft« sortiert werden können. Links im Streudiagramm
visualisieren wir die Autos mit ihren Eigenschaften `Kilometerstand [km]` und
`Preis [EUR]` als Punkte. Auf der rechten Seite werden wir schrittweise den
Entscheidungsbaum entwickeln. Ein Entscheidungsbaum visualisiert
Entscheidungsregeln in Form einer Baumstruktur. Zu Beginn wurde noch keine Frage
gestellt und alle Autos befinden sich gemeinsam in einem **Knoten** des
Entscheidungsbaumes, der visuell durch einen rechteckigen Kasten symbolisiert
wird. Dieser erste Knoten wird als **Wurzelknoten** bezeichnet, da er die Wurzel
des Entscheidungsbaumes darstellt. 

<img src="pics/combined_decisiontree00.svg" 
alt="Entscheidungsbaum - Start" 
class="image169"
width=100%>

Dann wird eine erste Frage gestellt. Ist der Verkaufspreis kleiner oder gleich
16376.50 EUR? Entsprechend dieser Entscheidung werden die Autos in zwei Gruppen
aufgeteilt. Wenn ja, wandern die Autos nach links und ansonsten nach rechts. Im
Entscheidungsbaum wird diese Aufteilung durch einen **Zweig** nach links und
einen Zweig nach rechts symbolisiert. Ein alternativer Name für Zweig ist
**Kante**. Die Autos »rutschen« die Zweige/Kanten entlang und landen in zwei
separaten Knoten. Im Streudiagramm entspricht diese Fragestellung dem Vergleich
mit einer horizontalen Linie bei y = 16376.5. Die gesamte Fläche unterhalb
dieser Linie wird blau markiert.

<img src="pics/combined_decisiontree01.svg" 
alt="Entscheidungsbaum - 1. Entscheidung" 
class="image169"
width=100%>

Bei den Autos mit einem Preis kleiner oder gleich 16376.50 EUR müssen wir nicht
weiter sortieren bzw. weitere Fragen stellen. Da aus diesem Knoten keine Zweige
mehr wachsen, wird dieser Knoten auch **Blatt** genannt. Aber in dem Knoten des
rechten Zweiges befinden sich fünf rote (also verkaufte) Autos und ein blaues
(also nicht verkauftes) Auto. Wir wollen diese Autos durch weitere Fragen
sortieren. Doch obwohl nur ein Auto (nämlich Auto 3) aus dieser Gruppe separiert
werden soll, ist dies nicht durch nur eine einzige Frage möglich. Lautet die
Frage: »Ist der Preis kleiner oder gleich 17300 EUR?«, dann wandern das rote
Auto 8 und das blaue Auto 3 nach links. Wählen wir die Frage: »Ist der
Kilometerstand kleiner oder gleich 13500 km?«, dann wandern ebenfalls Auto 3 und
Auto 8 nach links. Beide Fragen sind also gleichwertig, welches sollen wir
nehmen? Wir gehen nach der Reihenfolge der Eigenschaften vor. Da der
Kilometerstand in der Tabelle in der ersten Spalte steht und der Preis in der
zweiten Spalte, entscheiden wir uns für die Frage nach dem Kilometerstand.
  
<img src="pics/combined_decisiontree02.svg" 
alt="Entscheidungsbaum - 2. Entscheidung" 
class="image169"
width=100%>

Jetzt sind aber nur noch zwei Autos im linken Knoten, so dass diesmal eine
weitere Frage ausreicht, die beiden Autos in zwei Klassen zu sortieren. Wir
fragen: »Ist der Kilometerstand kleiner oder gleich 8198 km?«
   
<img src="pics/combined_decisiontree03.svg" 
alt="Entscheidungsbaum - 3. Entscheidung" 
class="image169"
width=100%>

Alle Autos sind nun durch die Fragen sortiert und befinden sich in Blättern.

```{admonition} Was ist ... ein Entscheidungsbaum?
Ein Entscheidungsbaum (Decision Tree) ist ein Modell zur Entscheidungsfindung,
das Daten mit Hilfe einer Baumstruktur sortiert. Die Datenobjekte starten beim
Wurzelknoten und werden dann über Knoten (=Entscheidungen) und Zweige/Kanten (=
Ergebnis der Entscheidung) in Blätter sortiert.
```


## Entscheidungsbäume mit Scikit-Learn

In der Praxis verwenden wir die ML-Bibliothek Scikit-Learn, um einen
Entscheidungsbaum zu trainieren. Das Modul [Scikit-Learn →
Tree](https://scikit-learn.org/stable/modules/tree.html) stellt sowohl einen
Entscheidungsbaum-Algorithmus für Klassifikationsprobleme als auch einen
Algorithmus für Regressionsprobleme zur Verfügung. Für das obige Beispiel
Autohaus importieren wir den Algorithmus für Klassifikationsprobleme namens
`DecisionTreeClassifier`:

```{code-cell}
from sklearn.tree import DecisionTreeClassifier
```

Dann erzeugen wir ein noch untrainiertes Entscheidungsbaum-Modell und weisen es
der Variable `modell` zu:

```{code-cell}
modell = DecisionTreeClassifier()
```

Bei der Erzeugung könnten wir noch verschiedene Optionen einstellen, die in der
[Dokumentation Scikit-Learn →
DecisionTreeClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html#sklearn.tree.DecisionTreeClassifier)
nachgelesen werden können. Zunächst belassen wir es aber bei den
Standardeinstellungen.

Als nächstes adaptieren wir die Daten aus dem Pandas-DataFrame so, dass das
Entscheidungsbaum-Modell trainiert werden kann. Der `DecisionTreeClassifier`
erwartet für das Training zwei Argumente. Als erstes Argument müssen die
Eingabedaten übergeben werden, also die Eigenschaften der Autos. Als zweites
Argument erwartet der `DecisionTreeClassifier` die Zielgröße, also den Status
»nicht verkauft« oder »verkauft«. Wir trennen daher den Pandas-DataFrame `daten`
auf und verwenden die Bezeichnung `X` für die Eingabedaten und `y` für die
Zielgröße.

```{code-cell}
X = daten[['Kilometerstand [km]', 'Preis [EUR]']]
y = daten['verkauft']
```

Als nächstes wird der Entscheidungsbaum trainiert. Dazu wird die Methode
`.fit()` mit den beiden Argumenten `X` und `y` aufgerufen.

```{code-cell}
modell.fit(X,y)
```

Jetzt ist zwar der Entscheidungsbaum trainiert, doch wir sehen nichts. Als
erstes überprüfen wir mit der Methode `.score()`, wie gut die Prognose des
Entscheidungsbaumes ist.

```{code-cell}
score = modell.score(X,y)
print(score)
```

Eine 1 steht für 100 %, also alle 10 Autos werden korrekt klassifiziert. Dazu hat der `DecisionTreeClassifier` basierend auf den Eingabedaten `X` eine Prognose erstellt und diese Prognose mit `y` verglichen. Für die Trainingsdaten funktioniert der Entscheidungsbaum also perfekt. Ob der Entscheidungsbaum ein neues, elftes Auto korrekt klassifizieren würde, kann so erst einmal nicht entschieden werden.

Zuletzt lassen wir den Entscheidungsbaum noch visualisieren. Dazu verwenden wir
die Funktion `plot_tree`, die zuerst aus dem Modul `sklearn.tree` importiert
wird. Als Argument übergeben wir das trainierte Modell. Zusätzlich setzen wir
für das optionale Argument `feature_names=` noch eine Liste mit den Namen der
Eigenschaftsnamen ein, so dass in der Visualisierung des Entscheidungsbaumes
direkt die Eigenschaften angezeigt werden. 

```{code-cell}
from sklearn.tree import plot_tree
plot_tree(modell, feature_names=['Kilometer [km]','Preis [EUR]']);
```

Weitere Details zu den Optionen der `plot_tree`-Funktion finden Sie in der
[Dokumentation Scikit-Learn →
plot_tree](https://scikit-learn.org/stable/modules/generated/sklearn.tree.plot_tree.html).

## Zusammenfassung und Ausblick

TODO
