# 5.5 Abstände

In diesem Kapitel vertiefen wir das Thema Lagebeziehungen von Geraden und Ebenen
weiter. Falls Geraden und Ebenen parallel liegen oder windschief sind, ist die
Information, welchen kürzesten Abstand die Objekte zueinander haben, relevant.
Daher beschäftigen wir uns in diesem Kapitel mit Abstandsberechnungen.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie können den Abstand eines Punktes zu einer Ebene berechnen.
* Sie können den Abstand eines Punktes zu einer Geraden berechnen.
* Sie können den Abstand von Geraden zueinander berechnen.
* Sie können den Abstand von Geraden zu Ebenen berechnen.
* Sie können den Abstand zweier Ebenen zueinander berechnen.
```

## Abstand eines Punktes zu einer Ebene

Liegt die Ebenengleichung in der hesseschen Normalform vor, ist die Berechnung
des Abstandes zwischen einem Punkt $Q$ und der Ebene $E$ recht einfach. Wir
setzen also voraus, dass die Ebene beschrieben wird durch

$$E: \vec{n}\cdot \left(X - P\right) = 0,$$

wobei $\vec{n}$ ein normierter Normalenvektor der Ebene ist, also $|\vec{n}|=1$
gilt, und $P$ ein Punkt der Ebene ist. Dann wird der Abstand $d(Q,E)$ von $Q$
zur Ebene $E$ berechnet, indem $Q$ für $X$ eingesetzt wird:

$$d(Q, E) = \vec{n}\cdot \left(Q - P\right).$$

Das Ergebnis $d(Q, E)$ kann positiv oder negativ sein. Ist $d(Q, E) > 0$
positiv, dann liegt der Punkt $Q$ auf der Seite der Ebene, in die der
Nromalenvektor zeigt. Ist $d(Q, E) < 0$ negativ, dann liegt $Q$ auf der anderen
Seite. Sollte $d(Q,E) = 0$ gelten, liegt der Punkt $Q$ in der Ebene.

```{dropdown} Video "Abstand eines Punktes von einer Ebene" von Flip the Classroom
<iframe width="560" height="315" src="https://www.youtube.com/embed/lmA1nLcsrbo?si=gGXHKUAbzC-KxDSf"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Kürzester Abstand Punkt Ebene berechnen" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/Z5OZ3QKUAWE?si=WHh_-F25iY5ZPTcS"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Abstand Punkt zur Ebene" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/H4aimQQs694?si=4jXGXsLFHFd3Ynf1"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Abstand eines Punktes zu einer Geraden

Es gibt verschiedene Möglichkeiten, den Abstand eines Punktes $Q$ zu einer
Geraden $g: P + s\cdot\vec{v}$ zu berechnen. Eine einfache Möglichkeit ist, eine
Hilfsebene folgendermaßen zu konstruieren:

1. Der Punkt $Q$ liegt in der Hilfsebene $E$.
2. Der Normalenvektor $\vec{n}$ entspricht dem Richtungsvektor der Geraden
   $\vec{v}$.

Dann genügt es, den Schnittpunkt der Geraden mit der Hilfsebene zu berechnen,
den wir $L$ nennen. Der Abstand von $L$ zu $Q$ ist der gesuchte Abstand. Warum
haben wir den Punkt ausgerechnet $L$ genannt? Mit Abstand ist der kürzeste
Abstand des Puntkes $Q$ zur Geraden gemeint. Dieser Abstand wird **Lot** genannt
und dementsprechend ist der Schnittpunkt der Geraden mit der Hilfsebene der
**Lotfußpunkt**.

```{dropdown} Video "Abstand eines Punktes von einer Geraden" von Flip the Classroom
<iframe width="560" height="315" src="https://www.youtube.com/embed/0q796DzcXVU?si=KVfi64HzZc7B5TGt"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Abstand zwischen Punkt und Gerade" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/sURUSsz7O9s?si=e-PIyPhmItTEAVYt"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Abstand Punkt Gerade" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/J0OI6gxaqSE?si=0-E0kDx2OiathAZ-"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Abstand einer Geraden zu einer Geraden

Von den vier möglichen Fällen, wie eine Gerade zu einer Gerade liegen kann, sind
für Abstandsberechnungen die beiden Fälle parallele Geraden oder windschiefe
Geraden relevant. In den beiden anderen Fällen ist der Abstand Null.

### Fall: parallele Geraden

Sind die Gerade $g_1: X = P_1 + s\cdot\vec{v}$ und $g_2: X = P_2 + t
\cdot\vec{v_2}$ parallel, dann nehmen wir einen beliebigen Punkt der Geraden
$g_1$ und berechnen den Abstand von diesem Punkt zur Gerade $g_2$. Das kann
beispielsweise der Punkt $P_1$ sein.

```{dropdown} Video "Abstand parallele Geraden" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/YW5r7XAZJH4?si=VblLFF5o8vk6hpkH"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

### Fall: windschiefe Geraden

Sind die Gerade $g_1: X = P_1 + s\cdot\vec{v}$ und $g_2: X = P_2 + t
\cdot\vec{v_2}$ windschief, dann gehen wir folgendermaßen vor. Wir konstruieren
eine Hilfsebene $E$, die $g_1$ enthÄlt und parallel zu $g_2$ ist. Das geht
beispielsweise, indem man den Normalenvektor $\vec{n} =
\vec{v_1}\times\vec{v_2}$ nimmt. Dann ermittelt man einen beliebigen Punkt $P$
auf $g_2$ (z.B. $P_2$) und berechnet den Abstand dieses Punktes zu $E$.

```{dropdown} Video "Abstand windschiefer Geraden" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/bRmp7I-TV2Q?si=zY80xSbqsjkXJS3Q"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Abstand einer Geraden zu einer Ebene

Betrachten wir eine Gerade, die in einer Ebene liegt oder eine Ebene durchstößt,
dann ist der Abstand Null. Relevant ist bei der Abstandsberechnung einer Geraden
zu einer Ebene nur der Fall, wenn die Gerade parallel zur Ebene liegt. Dann
genügt es aber auch, einen beliebigen Punkt der Gerade zu nehmen und seinen
Abstand zur Ebene zu berechnen.

## Abstand einer Ebenen zu einer Ebene

Auch hier ist nur der Fall relevant, wenn die beiden Ebenen parallel zueinander
liegen. Auch hier genügt es, einen beliebigen Punkt der ersten Ebene zu nehmen
und seinen Abstand zur zweiten Ebene zu berechnen. Schneiden sich higegen die
beiden Ebenen oder sind sie identisch, ist ihr Abstand Null.

## Zusammenfassung und Ausblick

In diesem Kapitel haben wir die Analyse der LAgebeziehungen von Geraden und
Ebenen vertieft, indem wir die Abstände von ihnen berechnen, sofern sie sich
nicht schneiden und nicht identisch sind. Im nächsten Kapitel werden wir uns
damit beschäftigen, welchen Winkel sie zueinander haben, wenn sie sich
schneiden.
