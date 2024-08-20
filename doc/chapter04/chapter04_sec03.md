# 4.3 Geometrische Interpretation Skalarprodukt

```{admonition} Warnung
:class: warning
Dieser Teil des Vorlesungsskriptes wird gerade überarbeitet.
```

In diesem Kapitel werden wir das Skalarprodukt für Vektoren in der Geometrie
anwenden.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie kennen den Zusammenhang zwischen Skalarprodukt und Betrag/Länge eines
  Vektors: 

  $$|\vec{a}|=\sqrt{\vec{a}\cdot\vec{a}}.$$

* Sie wissen, wie das **Skalarprodukt** zweier Vektoren **geometrisch**
  definiert ist: Das Skalarprodukt der Vektoren $\vec{a}$ und $\vec{b}$
  ist das Produkt aus den Längen der beiden Vektoren und dem Kosinus des von den
  beiden Vektoren eingeschlossenen Winkels $\varphi = \angle (\vec{a},\vec{b})$:

  $$\vec{a}\cdot\vec{b} = |\vec{a}|\cdot|\vec{b}| \cdot \cos(\varphi).$$

* Sie können den Winkel zwischen zwei Vektoren berechnen, wenn Sie das
  Skalarprodukt und die beiden Längen kennen:

  $$\varphi = \arccos\left(\frac{\vec{a}\cdot\vec{b}}{|\vec{a}|\cdot|\vec{b}|}\right).$$

* Sie können anhand des Vorzeichens des Skalarproduktes Aussagen über die
  Orientierung der Vektorn zueinander treffen.
```

## Skalarprodukt und Betrag von Vektoren

Die Länge einer Verschiebung oder einer Bewegung ist gleich dem Betrag des
Vektors $\vec{a}\in\mathbb{R}^n$, der defininiert ist als

$$|\vec{a}| = \sqrt{a_1^2 + a_2^2 + \ldots + a_n^2}.$$

Mit Hilfe des Skalarproduktes können wir die Länge bzw. den Betrag auch
folgendermaßen berechnen:

$$|\vec{a}|=\sqrt{\vec{a}\cdot\vec{a}}.$$

```{dropdown} Video "Zusammenhang Skalarprodukt und Länge Vektor" von Mathehoch13
<iframe width="560" height="315" src="https://www.youtube.com/embed/Zjc7aI8cp4o?si=EMLwSAnLYt8aC01V" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Skalarprodukt und eingeschlossener Winkel

Als nächstes führen wir den eingeschlossenen Winkel zwischen zwei Vektoren ein.
Geometrisch interpretieren wir die beiden Vektoren $\vec{a}\in\mathbb{R}^n$ und
$\vec{b}\in\mathbb{R}^n$ als Bewegungen, die beide an einem gemeinsamen Punkt
starten. Unabhängig von der Reihenfolge der Vektoren wird der Winkel zwischen
den beiden Richtungen, in die der Startpunkt verschoben werden soll, als der
Winkel der Vektoren $\vec{a}$ und $\vec{b}$ bezeichnet. Er ist stets der
kleinere der möglichen Winkel und liegt somit zwischen 0 und 180° bzw. zwischen
0 und $\pi$ im Bogenmaß. Wir verwenden dazu das Symbol $\angle
(\vec{a},\vec{b})$ oder den griechischen Buchstaben Phi $\varphi$.

Für den zwischen $\vec{a}$ und $\vec{b}$ eingeschlossenen Winkel $\varphi$ gilt
die Beziehung

$$\vec{a}\cdot\vec{b} = |\vec{a}|\cdot|\vec{b}| \cdot \cos(\varphi).$$

Das Skalarprodukt der Vektoren $\vec{a}$ und $\vec{b}$ kann über die
Beträge/Längen der Vektoren $|\vec{a}|$ und $|\vec{b}|$ sowie dem Kosinus-Wert
des eingeschlossenen Winkels $\varphi = \angle (\vec{a},\vec{b})$ berechnet
werden. Das ermöglicht direkt einige Aussagen über die Orientierung der Vektoren
zueinander. Darüber hinaus können wir, sofern die beiden Vektoren $\vec{a}$ und
$\vec{b}$ nicht der Nullvektor sind, auch mit der Arkuskosinus-Funktion den
Winkel $\varphi$ aus dem Skalarprodukt berechnen:

$$\varphi =
\arccos\left(\frac{\vec{a}\cdot\vec{b}}{|\vec{a}|\cdot|\vec{b}|}\right).$$

Aus dieser Beziehung können einige Schlussfolgerungen gezogen werden:

* Sind $\vec{a}$ und $\vec{b}$ parallel und gleichorientiert, ist also der
  eingeschlossene Winkel $\varphi = 0$, dann gilt

$$\vec{a}\cdot\vec{b} = |\vec{a}| \cdot |\vec{b}|.$$

* Sind $\vec{a}$ und $\vec{b}$ parallel und entgegengesetzt orientiert, gilt
  also für den eingeschlossenen Winkel $\varphi = \pi$, dann gilt

$$\vec{a}\cdot\vec{b} = - |\vec{a}| \cdot |\vec{b}|.$$

* Sind die beiden Vektoren $\vec{a}$ und $\vec{b}$ orthogonal (stehen senkrecht
  aufeinander), dann gilt

$$\vec{a}\cdot\vec{b} = 0.$$

* Ist $\varphi$ ein spitzer Winkel, so gilt

$$\vec{a}\cdot\vec{b} > 0.$$

* Ist $\varphi$ ein stumpfer Winkel, so gilt

$$\vec{a}\cdot\vec{b} < 0.$$

Es gilt

$$|\vec{a}\cdot\vec{b}| \leq |\vec{a}| \cdot |\vec{b}|.$$

Es gilt

$$|\vec{a}\cdot\vec{b}| = |\vec{a}| \cdot |\vec{b}| \Leftrightarrow \vec{a},
\vec{b} \text{ linear abhängig}.$$

Die große Bedeutung des Skalarproduktes in der Geometrie erkennen Sie daran, dass es sehr viele Erklärvideos zu diesem Thema gibt. Einige Videos zu dem Thema sind im Folgenden gelistet.

```{dropdown} Video "geometrische Interpretation Skalarprodukt" von Visual X
<iframe width="560" height="315" src="https://www.youtube.com/embed/swMhAjkoCm0?si=XPKYIezPvpQ7HqKf" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Winkel zwischen zwei Vektoren" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/vB9yjxpbDQ4?si=QIH86HSQJf915iRr" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Standard Skalarprodukt Einfach Erklärt" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/wJAniAr6avU?si=E2-wbANRbD2VElRh" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Skalarprodukt Teil 2 |  Erklärung & Bedeutung" von Einfach Mathe!
<iframe width="560" height="315" src="https://www.youtube.com/embed/rZ1zS3MBV0Y?si=0SEe5f51bsH965WF" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Skalarprodukt II" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/uGs7vGAxJko?si=YYM3r12agb-6C_tf" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

In diesem Kapitel haben wir die geometrische Interpretation des Skalarproduktes
kennengelernt. Einige Autoren von Mathematikbüchern gehen den umgekehrten Weg
und definieren das Skalarprodukt über die Formel $\vec{a}\cdot\vec{b} =
|\vec{a}|\cdot|\vec{b}| \cdot \cos(\varphi)$. Im nächsten Kapitel werden wir die
Anwendungen des Skalarproduktes in der Geometrie (und damit in Physik und
Technische Mechanik) weiter vertiefen.
