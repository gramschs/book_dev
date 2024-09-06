# 5.2 Ebenen

Eine Ebene ist ein zweidimensionales, flaches Gebilde im Raum, das unendlich
ausgedehnt ist. In diesem Kapitel werden wir zwei Varianten kennenlernen, Ebenen
mathematisch zu beschreiben, nämlich die Parametergleichung und die
Normalengleichung.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie können eine Ebene durch ihre **Parametergleichung** beschreiben.
* Sie können eine Ebene durch ihre **Normalengleichung** beschreiben.
```

## Parametergleichung der Ebene

Die Lage einer Ebene im dreidimenionalen Raum $\mathbb{R}^3$ kann man durch
verschiedene Angaben eindeutig festlegen. Beispielsweise genügt es drei Punkte
anzugeben, wobei der dritte Punkt nicht auf der Geraden durch die ersten beiden
Punkte liegen darf. Wir nennen diese Punkte im Folgenden $P$, $Q$ und $R$. Wir
können den Verbindungsvektor $\vec{u} := \overrightarrow{PQ}$ zwischen $P$ und
$Q$ bilden und den Verbindungsvektor $\vec{v}:=\overrightarrow{PR}$ zwischen $P$
und $R$. Jeder Punkt der Ebene kann dann erreicht werden, indem wir den Punkt
$P$ um Vielfache in die erste Richtung $\vec{u}$ und um Vielfache in die zweite
Richtung $\vec{v}$ verschieben. Formal aufgeschrieben erhalten wir

$$X = s\cdot\vec{u} + t\cdot\vec{v}.$$

Wie bei der Parametergleichung der Ebene nennen wir die beiden reellen Zahlen
$s$ und $t$ **Parameter der Ebenengleichung**. Für jede Kombination von Werten
$s\in\mathbb{R}$ und $t\in\mathbb{R}$ erhalten wir einen anderen Punkt in der
Ebene und umgekehrt gehört zu jedem Punkt der Ebene ein eindeutiges Paar von
Parametern $(s,t)$. Manchmal wird die Ebenengleichung daher auch als

$$X(s,t) = s\cdot\vec{u} + t\cdot\vec{v}$$

notiert.

```{admonition} Wie lautet ... die Parametergleichung der Ebene?
:class: admonition
Eine Ebene ist eine Menge von Punkten $X\in\mathbb{R}^3$, die sich schreiben
lässt als

$$E = \{ X \in\mathbb{R}^3 \,|\, X = s\cdot\vec{u} + t\cdot\vec{v}\}.$$

Die Skalare $s\in\mathbb{R}$ und $t\in\mathbb{R}$ werden Parameter genannt und
die beiden Vektoren $\vec{u}\in\mathbb{R}^3$ und $\vec{v}\in\mathbb{R}^3$
Richtungsvektoren. Wir schreiben auch kurz $E: X = s\cdot\vec{u} +
t\cdot\vec{v}$ und nennen diese Darstellung Parametergleichung der Ebene.
```

## Normalengleichung der Ebene

Alternativ kann eine Ebene auch durch einen Punkt $P$, der in der Ebene liegt,
und den sogenannten **Normalenvektor** beschrieben werden. Ein Normalenvektor
ist ein Vektor, der senkrecht auf der Ebene steht. Damit ist gemeint, dass zwei
beliebige Punkte der Ebene verbunden werden können und dieser Verbindungsvektor
orthogonal zum Normalenvektor ist.

Wir nennen jetzt allgemein irgendeinen Punkt der Ebene $X$. Laut obiger
Überlegung ist also der Verbindungsvektor $\overrightarrow{PX} = X - P$
orthogonal zum Normalenvektor $\vec{n}$. Zwei Vektoren sind orthogonal
zueinander, wenn ihr Skalarprodukt Null ist. In mathematischer Notation gilt
also:

$$\vec{n}\perp\overrightarrow{PX}  \; \Leftrightarrow \;
\vec{n}\cdot\overrightarrow{PX}=0.$$

Drücken wir den Verbindungsvektor $\overrightarrow{PX}$ als Differenz der beiden
Punkte $X$ und $P$ aus, erhalten wir die **Normalengleichung der Ebene**

$$\vec{n}\cdot (X-P)=0.$$

Diese Gleichung lässt sich nicht explizit nach $X$ auflösen. Die Punkte der
Ebene werden also nur indirekt charakterisiert.

```{admonition} Was ist ... die Normalengleichung der Ebene?
:class: note
Eine Ebene ist eine Menge von Punkten $X\in\mathbb{R}^3$, die sich schreiben
lässt als

$$E = \{X \,|\, \vec{n}\cdot (X-P) = 0\}.$$

Der Vektor $\vec{n}\in\mathbb{R}^3$ wird Normalenvektor genannt und
$P\in\mathbb{R}^3$ ist ein Punkt, der in der Ebene liegt. Wir schreiben auch
kurz $E: \vec{n}\cdot (X-P) = 0$ und nennen diese Darstellung Normalengleichung
der Ebene.
```

## Videos

Die folgenden Videos erklären die beiden Darstellungsformen erneut. Meist wird
nicht strikt zwischen Punkten und Vektoren unterschieden.

```{dropdown} Video "Parameterdarstellung Ebene" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/xgn1c3SAKZI"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Parameterdarstellung Ebene drei Punkte" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/aUohWmcs3Dc"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Normalendarstellung Ebene" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/GoqI8uG6PYI"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Umwandlung Parameter- zur Normalendarstellung" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/0Hg56BoiHq0"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Ebenengleichung aus drei Punkten" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/TsyHJ2P4qOA"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Parameterform Koordinatenform" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/xv1UOakv3XI"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

Nachdem wir nun die Gleichungen für Geraden und Ebenen gelernt haben, möchten
wir als nächstes untersuchen, wie die Lage der Geraden und Ébenen zueinander
ist. Bevor wir uns dieses Thema im übernächsten Kapitel erarbeiten, beschäftigen
wir uns aber zunächst mit dem systematischen Lösen von linearen
Gleichungssystemen. Das werden wir brauchen, um beispielsweise Schnittpunkte von
Geraden und Ebenen berechnen zu können.
