# 4.6 Spatprodukt

Das Vektorprodukt existiert nur im dreidimensionalen Standardvektorraum
$\mathbb{R}^3$, weil es aufgrund seiner geomtrischen Bedeutung (orthogonal zu
den beiden aufspannenden Vektoren, Länge entsprich Flächeninhalt des
Parallelogramms) eingeführt wurde. Auch das Spatprodukt existiert nur im
$\mathbb{R}^3$. Es beschreibt das orientierte Volumen eines Spats.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie wissen, was ein **Spat** ist.
* Sie können das **Spatprodukt** dreier Vektoren in Koordinaten ausrechnen.
* Sie wissen, dass das Spatprodukt das **orientierte Volumen** des Spats angibt.
```

## Was ist ein Spat?

Ein Spat ist sozusagen die Erweiterung eines Parallelogramms in die dritte
Richtung. Ein Spat ist ein geometrischer Körper, der durch sechs Parallelogramme
begrenzt wird. Von den sechs Parallelogrammen sind jeweils die beiden
gegenüberliegenden deckungsgleich und liegen in parallelen Ebenen. Am
einfachsten ist es, hier ein Bild zu betrachten.

```{figure} pics/spat.svg
---
width: 50%
name: spat
---
Spat, Quelle: [Wikimedia
Commons](https://de.wikipedia.org/wiki/Spatprodukt#/media/Datei:Parallelepiped2.svg) von
Ag2gaeh, Lizenz: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0)
```

## Spatprodukt

Sind $\vec{a}$, $\vec{b}$ und $\vec{c}$ drei Vektoren, die einen Spat
aufspannen, so wird das Spatprodukt gebildet als

$$\left(\vec{a}\times\vec{b}\right)\cdot\vec{c}.$$

Oft wird für das Spatprodukt das Symbol $[ \; ]$ genutzt, also

$$[\vec{a}, \vec{b}, \vec{c}] =
\left(\vec{a}\times\vec{b}\right)\cdot\vec{c}.$$

Das Spatprodukt ist *nicht kommutativ*. Vertauscht man hingegen die Vektoren
$\vec{a}$, $\vec{b}$ und $\vec{c}$ **zyklisch**, dann ändert sich der Wert des
Spatproduktes nicht. Es gilt also

$$\left(\vec{a}\times\vec{b}\right)\cdot\vec{c} =
\left(\vec{b}\times\vec{c}\right)\cdot\vec{a} =
\left(\vec{c}\times\vec{a}\right)\cdot\vec{b}.$$

## Geometrische Interpretation des Spatproduktes

Das Spatprodukte wurde hauptsächlich wegen seiner geometrischen Interpretation
eingeführt. Es gibt das **orientierte Volumen** des Spats an. Betrachten wir
zunächst den Betrag des Skalarproduktes, dann erhalten wir das Volumen des
Spats:

$$V = \left| \left(\vec{a}\times\vec{b}\right)\cdot\vec{c} \right|\,.$$

Lassen wir hingegen den Betrag weg, dann kann das Spatprodukt auch negative
Werte annehmen. Ist $\left(\vec{a}\times\vec{b}\right)\cdot\vec{c}$ negativ,
bilden die Vektoren $\vec{a}$, $\vec{b}$ und $\vec{c}$ ein **Linkssystem**. Ist
hingegen das Spatprodukt positiv, so bilden die drei Vektoren ein
**Rechtssystem**.

```{dropdown} Video "Spatprodukt" von Daniel Jung
<iframe width="560" height="315" src="https://www.youtube.com/embed/plM5HpVjycE" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

Mit Skalarprodukt, Vektorprodukt und Spatprodukt haben wir drei verschiedenen
Rechenoperationen für |Vektoren kennengelernt. In den folgenden Kapiteln werden
wir Vektoren und diese Rechenoperationen nutzen, um Geraden und Ebenen sowie
deren Lage im Raum zu beschreiben.
