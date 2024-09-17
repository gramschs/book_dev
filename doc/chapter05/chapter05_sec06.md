# 5.6 Winkel

Schneiden sich Gerade und Gerade oder Gerade und Ebene in einem Schnittpunkt
bzw. Ebene und Ebene in einer Schnittgeraden, ist die Frage interessant, welchen
Winkel diese Objekte zueinander einnehmen. In diesem Kapitel werden wir uns mit
diesen drei Fällen beschäftigen und die dazugehörigen Winkel berechnen.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie können den Winkel zwischen zwei Geraden berechnen.
* Sie können den Winkel zwischen einer Gerade und einer Ebene berechnen.
* Sie können den Winkel zwischen zwei Ebenen berechnen.
```

## Winkel zwischen zwei Geraden

Schneiden sich zwei Geraden $g_1$ und $g_2$ in einem Schnittpunkt, treten zwei
verschiedene Winkel auf. Hier in der Skizze sind diese mit $\alpha$ und $\beta$
gekennzeichnet.

```{figure} pics/schnittwinkel_geraden.png
---
width: 50%
name: schnittwinkel_geraden
---
Winkel zwischen zwei Geraden; Quelle: eigene Darstellung; 
Lizenz: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0)
```

Als **Schnittwinkel zweier Geraden** mit dem mathematischen Symbol
$\angle(g_1,g_2)$ definieren wir den kleineren der beiden Winkel. Um den
Schnittwinkel zu berechnen, können wir den Winkel zwischen den beiden
Richtungsvektoren der Geraden berechnen. Ist die erste Geradengleichung gegeben
als $g_1: X = P_1 + s\cdot\vec{v_1}$ und die zweite Geradengleichung als $g_2: X
= P_2 + t\cdot\vec{v_2}$, dann können wir die geometrische Interpretation des
Skalarproduktes nutzen:

$$\cos(\varphi) = \frac{\vec{v_1}\cdot\vec{v_2}}{|\vec{v_1}| \cdot
|\vec{v_2}|}.$$

Dabei ist $\varphi=\angle(\vec{v_1},\vec{v_2})$ der zwischen den beiden
Richtungsvektoren $\vec{v_1}$ und $\vec{v_2}$ eingeschlossene Winkel. Ist das
Skalarprodukt positiv, ist der Winkel spitz und entspricht dem kleineren Winkel,
also dem gesuchten Schnittwinkel. Ist das Skalarprodukt negativ, haben wir den
stumpfen Winkel. Um diese Fallunterscheidung zu umgehen, bilden wir zuerst den
Betrag des Skalarproduktes und können dann die Umkehrfunktion Arkuskosinus
nutzen. Damit lautet die Formel zur Berechnung des Schnittwinkels
$\angle(g_1,g_2)$:

$$\angle(g_1,g_2) = \arccos\left(\frac{|\vec{v_1}\cdot\vec{v_2}|}{|\vec{v_1}| \cdot
|\vec{v_2}|}\right).$$

```{dropdown} Video "Winkel zwischen zwei Geraden" von Cornelsen
<iframe width="560" height="315"
src="https://www.youtube.com/embed/PYkoKh99Yw0?si=lnYyvBkEnkrMLtpd"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Schnittpunkt und Schnittwinkel berechnen" von MathePeter
<iframe width="560" height="315"
src="https://www.youtube.com/embed/oopcNiZa5x8?si=soRvDvjhOb7rdIrc"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Winkel zwischen Gerade und Ebene

Möchten wir den Winkel zwischen einer Gerade und einer Ebene berechnen, nehmen
wir den Richtungsvektor der Geraden und den Normalenvektor der Ebene.
Angenommen, die Geradengleichung lautet $g: X = P + s\cdot\vec{v}$ und ein
Normalenvektor der Ebene ist $\vec{n}$. Der gesuchte Schnittwinkel zwischen der
Gerade und der Ebene soll $\varphi$ heißen. Dann wissen wir, dass der Winkel
zwischen dem Normalenvektor und dem Richungsvektor der Geraden gerade
$90^{\circ}-\varphi$ ist. Um uns erneut Fallunterscheidungen zwischen spitzen
und stumpfen Winkel zu ersparen, nehmen wir auch hier den Betrag des
Skalarproduktes:

$$\cos(90^{\circ}-\varphi) = \frac{|\vec{v}\cdot\vec{n}|}{|\vec{v}|\cdot
|\vec{n}|}.$$

Wir könnten nun erneut den Arkuskosinus anwenden und dann die entstehende
Gleichung nach dem gesuchten Schnittwinkel $\varphi$ auflösen. Da aber
$\cos(90^{\circ}-\varphi)=\sin(\varphi)$ gilt, können wir auch direkt den
Schnittwinkel über die Formel

$$\angle(g,E) = \arcsin\left(\frac{|\vec{v}\cdot\vec{n}|}{|\vec{v}| \cdot
|\vec{n}|}\right)$$

berechnen.

```{dropdown} Video "Winkel zwischen Gerade und Ebene" von Mathematrick
<iframe width="560" height="315"
src="https://www.youtube.com/embed/R6CzF989qOo?si=tRmJknmNSJGL16Z8"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Winkel Gerade - Ebene" von MathePeter
<iframe width="560" height="315"
src="https://www.youtube.com/embed/CqBSmBOd4xM?si=pVXTBXbVqVC8Fhji"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Winkel zwischen Ebene und Ebene

Soll der Schnittwinkel zweier Ebenen berechnet werden, werden von beiden Ebenen
Normalenvektoren genommen. $\vec{n_1}$ bezeichne einen Normalenvektor der ersten
Ebene und $\vec{n_2}$ einen Normalenvektor der zweiten Ebene. Dann gilt wiederum
für den Schnittwinkel

$$\angle(E_1,E_1) = \arccos \left(\frac{|\vec{n_1}\cdot\vec{n_2}|}
{|\vec{n_1}|\cdot |\vec{n_2}|}\right).$$

```{dropdown} Video "Schnittwinkel" von Flip the Classroom
<iframe width="560" height="315"
src="https://www.youtube.com/embed/Qhz-zsdDZHI?si=c1cO5sm6nLNnG86N"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Winkel zwischen zwei Ebenen" von Mathematrick
<iframe width="560" height="315"
src="https://www.youtube.com/embed/ZC0SHn5UK-Y?si=6m80A2uc5-g_0PV-"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Winkel Ebene - Ebene" von MathePeter
<iframe width="560" height="315"
src="https://www.youtube.com/embed/q3V_ZRtx-Yc?si=CWi1w6_meHZsC5JH"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

Mit der Berechnung der Schnittwinkel schließen wir das Thema Punkte, Geraden und
Ebenen ab. Als nächstes werden wir uns mit Matrizen beschäftigen.
