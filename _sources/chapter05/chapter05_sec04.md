# 5.4 Lagebeziehungen Geraden und Ebenen

Nun werden wir uns mit der Lagebeziehung von Geraden und Ebenen beschäftigen.
DAbei berückscihtigen wir die drei möglichen Kombinationen:

* Gerade zu Gerade
* Gerade zu Ebene und
* Ebene zu Ebene.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie können berechnen, ob zwei Geraden
  * identisch sind,
  * parallel sind,
  * sich schneiden oder
  * windschief sind.
* Falls sich zwei Geraden schneiden, können Sie den Schnittpunkt der beiden
  Geraden bestimmen.
* Sie können berechnen, ob eine Gerade
  * in einer Ebene liegt,
  * parallel zur Ebene liegt oder
  * die Ebene schneidet.
* Falls eine Gerade eine Ebene schneidet, können Sie den Schnittpunkt von der
  Geraden mit der Ebenen bestimmen.
* Sie können berechnen, ob zwei Ebenen
  * identisch sind,
  * parallel sind oder
  * sich schneiden.
* Falls zwei Ebenen sich schneiden, können Sie die Schnittgerade der beiden
  Ebenen bestimmen.
```

## Gerade — Gerade

Im euklidischen Raum $\mathbb{R}^2$, also in der Ebene, gibt es drei
Möglichkeiten, wie zwei Geraden zueinander liegen. Sie können identisch sein,
sie können parallel verlaufen und sie können sich schneiden. Im
dreidimensionalen Raum $\mathbb{R}^3$ gibt es noch eine neue, vierte
Möglichkeit. Die Geraden können **windschief** sein. Dabei haben sie *keinen
Schnittpunkt*, sind aber trotzdem nicht parallel.

Eine erste Unterscheidungsmöglichkeit zwischen den Fällen identisch/parallel und
schneiden/windschief bietet die Analyse der Richtungsvektoren. Sind die beiden
Richtungsvektoren linear abhängig, dann sind die Geraden entweder identisch oder
echt parallel zueinander. Mit Hilfe einer Punktprobe kann dann leicht überprüft
werden, welcher der beiden Fälle vorliegt.

Sind die beiden Richtungsvektoren linear unabhängig, dann sind die beiden
Geraden entweder windschief oder sie schneiden sich. Welcher der beiden Fälle
vorliegt, lässt sich dann durch Gleichsetzen der beiden Parametergleichungen
entscheiden.

Wenn die erste Gerade in Parameterdarstellung $g_1: X = P_1 + s\cdot\vec{v_1}, \;
s\in\mathbb{R},$ lautet und die zweite Gerade $g_2: X = P_2 + t\cdot\vec{v_2}, \;
t\in\mathbb{R},$ dann bedeutet Gleichsetzen, dass die vektorielle Gleichung

$$P_1 + s\cdot\vec{v_1} = P_2 + t\cdot\vec{v_2}$$

gelöst werden soll. Lesen wir diese vektorielle Gleichung komponentenweise,
erhalten wir drei Gleichungen für zwei Parameter $s$ und $t$. Es liegt also ein
überbestimmtes lineares Gleichungssystem vor. Wir lösen das Gleichungssystem.
Die drei Möglichkeiten entsprechen den folgenden Lagebeziehungen:

1. Das Gleichungssystem hat keine Lösung. Dann sind die beiden Geraden parallel
   oder windschief. Wenn bereits der Test auf lineare Abhängigkeit durchgeführt
   wurde und gezeigt hat, dass die Richtungsvektoren linear abhängig sind, dann
   sind die Geraden parallel und ansonsten windschief.
2. Das Gleichungssystem hat unendlich viele Lösungen. Dann sind die beiden
   Geraden identisch.
3. Das Gleichungssystem hat eine eindeutige Lösung. Dann schneiden sich die
   beiden Geraden. Der Schnittpunkt kann dann berechnet werden, indem entweder
   die Lösung für $s$ in $g_1$ oder die Lösung für $t$ in $g_2$ eingesetzt wird.

Das folgende Video haben wir bereits eingeführt. Diesmal können Sie bei
Zeitmarke 3:20 min starten.

```{dropdown} Video "Geraden" von Flip the Classroom
<iframe width="560" height="315" src="https://www.youtube.com/embed/qCRN2Qsm0D0?si=h1t4YF-klJKZKv57"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Gerade — Ebene

Bei der Lagebeziehung Gerade zu Ebene gibt es drei Fälle:

1. Die Gerade liegt in der Ebene.
2. Die Gerade ist parallel zu der Ebene.
3. Die Gerade schneidet die Ebene, es gibt einen Schnittpunkt (Durchstoßpunkt).

Um zu bestimmen, welcher der drei Fälle vorliegt, setzen wir die
Geradengleichung und die Ebenengleichung gleich. Hat das entstehende
Gleichungssystem unendlich viele Lösungen, dann liegt die Gerade in der Ebene.
Hat das Gleichungssystem keine Lösung, so sind die beiden Objekte parallel
zueinander. Bei einer eindeutigen Lösung des linearen Gleichungssystems haben
Gerade und Ebene einen Schnittpunkt. Die lösung des Gleichungssystems werden
entweder in die Geradengleichung oder in die Ebenengleichung eingesetzt, um den
Schnittpunkt zu berechnen.

```{dropdown} Video "Gegenseitige Lage von Ebenen und Geraden" von Flip the Classroom
<iframe width="560" height="315" src="https://www.youtube.com/embed/dd1rzxF29Yw?si=luwsLswXcC6ZL41K"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Ebene — Ebene

Auch bei der Lagebeziehung zwischen zwei Ebenen gibt es drei Möglichkeiten. Hier
ist es sinnvoll, die beiden Ebenengleichungen als Normalengleichung zu benutzen.
Liegt eine oder beide Ebenengleichungen noch in der Parameterform vor, sollten
sie umgewandelt werden. Dann können wir die Normalenvektoren untersuchen.

* Sind die beiden Normalenvektoren linear abhängig. Dann sind die Ebenen
  entweder parallel oder identisch. Welcher der beiden Fälle vorliegt, kann mit
  der Punktprobe überprüft werden.
* Sind die beiden Normalenvektoren linear unabhängig, dann schneiden sich die
  Ebenen. Die Schnittgerade kann durch Gleichsetzen der beiden Ebenengleichung
  bestimmt werden.

```{dropdown} Video "Gegenseitige Lagen von Ebenen" von Flip the Classroom
<iframe width="560" height="315" src="https://www.youtube.com/embed/PzgF1Z99dyo?si=OLL1rJtSUn5SLza-"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Weiteres Lernmaterial

```{dropdown} Video "Lage von Geraden" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/S9m44EDVQ6M"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Schnitt und Winkel Gerade und Ebene" von Mathe Peter
<iframe width="560" height="315" src="https://www.youtube.com/embed/CqBSmBOd4xM"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Lagebeziehung Ebene - Ebene" von Mathe Peter
<iframe width="560" height="315" src="https://www.youtube.com/embed/q3V_ZRtx-Yc"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

In diesem Kapitel haben wir die Lage von Gerade zu Gerade, Geraden zu Ebenen und
Ebenen zu Ebenen untersucht. Im nächsten Kapitel werden wir den Abstand von
Geraden und Ebenen zueinander untersuchen.
