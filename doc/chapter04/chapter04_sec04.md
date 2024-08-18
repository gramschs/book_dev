# 4.4 Anwendungen Skalarprodukt

```{admonition} Warnung
:class: warning
Dieser Teil des Vorlesungsskriptes wird gerade überarbeitet.
```

## Lernziele

```{admonition} Lernziele 
:class: goals
* Sie kennen den Begriff **Orthogonalität** und können mit dem Skalarprodukt
  überpüfen, ob zwei Vektoren orthogonal $\perp$ (= senkrecht zueinander) sind.
```

## Orthogonalität und orthogonale Projektion

Zwei Vektoren $\vec{a}\in\mathbb{R}^n$ und $b\in\mathbb{R}^n$ sind genau dann
orthogonal, wenn ihr Skalarprodukt Null ist:

$$\vec{a}\perp\vec{b} \Leftrightarrow \vec{a}\cdot\vec{b}=0.$$

Die orthogonale Projektion von $\vec{b}$ auf die durch den Vektor
$\vec{a}\neq\vec{0}$ gegebene Richtung ist der Vektor

$$\vec{b}_{\vec{a}} =
\left(\frac{\vec{b}\cdot\vec{a}}{|\vec{a}|^2}\right)\vec{a}.$$