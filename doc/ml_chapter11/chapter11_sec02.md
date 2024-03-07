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

# 11.2 Scikit-Learn Tree 

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