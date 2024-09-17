# 8.2 Addition, Subtraktion und Multiplikation komplexer Zahlen

Komplexe Zahlen sind zusammengesetzte Zahlen, eine Kombination der reellen
Zahlen mit den imaginären Zahlen. In diesem Kapitel werden wir uns damit
beschäftigen, wie komplexe Zahlen addiert, subtrahiert und multipliziert werden.
Dabei werden wir auch auf die geometrische Interpretation dieser
Rechenoperationen in der Gaußschen Zahlenebene eingehen.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie können zwei komplexe Zahlen in der Normalform **addieren**.
* Sie können die Addition zweier komplexer Zahlen geometrisch in der Gaußschen
  Zahlenebene interpretieren.
* Sie können zwei komplexe Zahlen in der Normalform **subtrahieren**.
* Sie können die Subtraktion zweier komplexer Zahlen geometrisch in der
  Gaußschen Zahlenebene interpretieren.
* Sie können zwei komplexe Zahlen in der Normalform **multiplizieren**.
* Sie können die Multiplikation zweier komplexer Zahlen geometrisch in der
  Gaußschen Zahlenebene interpretieren.
```

## Addition komplexer Zahlen

Eine komplexe Zahl ist eine aus reellen und imaginären Zahlen zusammengesetzte
Zahl. Sollen jetzt zwei komplexe Zahlen addiert werden, werden die reellen
Zahlen mit den reellen Zahlen verrechnet und die imaginären Zahlen mit den
imaginären Zahlen.

**Beispiel:** Es sollen die beiden komplexen Zahlen $z_1 = 1.3 +
0.4\mathrm{i}$ und $z_2 =  0.3 + 1.3\mathrm{i}$ addiert werden. Dann ist die
Summe der beiden komplexen Zahlen

$$z_1 + z_2 = (1.3 + 0.3) + (0.4 \mathrm{i} + 1.3\mathrm{i}) = 1.6 + 1.7
\mathrm{i}.$$

Natürlich können wir die Addition zweier komplexen Zahlen in Normalform auch
allgemein formulieren. Für zwei komplexe Zahlen $z_1$ und $z_2$

\begin{align*}
z_1 &= a_1 + b_1 \mathrm{i}\\
z_2 &= a_2 + b_2 \mathrm{i}\\
\end{align*}

ist die Summe der beiden komplexen Zahlen wieder eine komplexe Zahl:

$$z_1 + z_2 = (a_1 + a_2) + (b_1 + b_2) \cdot \mathrm{i}.$$

Die beiden Realteile werden addiert $a_1 + a_2$ und die beiden Imaginärteile
$b_1 + b_2$ werden addiert.

Werden die beiden komplexen Zahlen in der Gaußschen Zahlenebene dargestellt, so
entspricht die Addition der komplexen Zahlen der Addition von zwei Vektoren.

```{admonition} Interaktiv: Addition komplexe Zahlen von "Hart und Trocken"
:class: seealso, toggle
Starten Sie das

[Applet "Addition komplexe
Zahlen"](https://www.hartundtrocken.de/my-product/interaktiv-addition-komplexer-zahlen/)

von "Hart und Trocken". Dort können Sie zwei komplexe Zahlen in der Gaußschen
Zahlenebene wählen, indem Sie die beiden blauen Punkte bewegen. Die Summe dieser
beiden komplexen Zahlen wird orange dargestellt.
```

```{dropdown} Video "Komplexe Zahlen - Gaußsche Zahlenebene Addition" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/i6-cZfAquxQ?si=9uskfEIUMUBTwfm9" title="YouTube video player" frameborder="0" allow="accelerometer;
autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

## Subtraktion komplexer Zahlen

Die Subtraktion zweier komplexer Zahlen funktioniert wird die Addition getrennt
für Realteil und Imaginärteil.

**Beispiel:** Es sollen die beiden komplexen Zahlen $z_1 = 1.3 + 0.4\mathrm{i}$
und $z_2 =  0.3 + 1.3\mathrm{i}$ subtrahiert werden. Dann ist die Differenz der
beiden komplexen Zahlen

$$z_1 - z_2 = (1.3 - 0.3) + (0.4 \mathrm{i} - 1.3\mathrm{i}) = 1 - 0.9
\mathrm{i}.$$

Allgemein formuliert ist die Differenz zweier komplexer Zahlen $z_1$ und $z_2$ mit

\begin{align*}
z_1 &= a_1 + b_1 \mathrm{i}\\
z_2 &= a_2 + b_2 \mathrm{i}\\
\end{align*}

die folgende komplexe Zahl:

$$z_1 - z_2 = (a_1 - a_2) + (b_1 - b_2) \cdot \mathrm{i}.$$

Die beiden Realteile werden subtrahiert $a_1 - a_2$ und die beiden Imaginärteile
$b_1 - b_2$ werden subtrahiert.

## Multiplikation komplexer Zahlen

Die Multiplikation zweier komplexer Zahlen ist nicht weiter schwer, wenn wir die Regel $\mathrm{i}^2 = -1$ beachten. Dann können wir einfach Ausmultiplizieren.

**Beispiel:** Die beiden komplexen Zahlen $z_1 = 2 + 3\mathrm{i}$ und $z_2 = -4 + 2\mathrm{i}$ sollen multipliziert werden. Dann gilt

\begin{align*}
z_1 \cdot z_2
&= (2 + 3\mathrm{i}) \cdot (-4 + 2\mathrm{i}) = \\
&= 2\cdot(-4) + 4\mathrm{i} - 12\mathrm{i} + 6 \mathrm{i}^2 = \\
&= -8 -8\mathrm{i} + 6\cdot(-1) = \\
&= -14 - 8\mathrm{i}.
\end{align*}

Allgmein können wir folgende Formel für die Multiplikation zweier komplexer
Zahlen notieren. Gegeben sind zwei komplexe Zahlen $z_1$ und $z_2$ mit

\begin{align*}
z_1 &= a_1 + b_1 \mathrm{i},\\
z_2 &= a_2 + b_2 \mathrm{i}.\\
\end{align*}

Dann ist das Produkt dieser beiden komplexen Zahlen die folgende Zahl:

$$z_1 \cdot z_2 = (a_1 + b_1\mathrm{i}) \cdot (a_2 + b_2\mathrm{i}) = (a_1 a_2 -
b_1 b_2) + (a_1 b_2 + b_1 a_2) \cdot\mathrm{i}.$$

Tatsächlich ist es aufwendiger, sich die Formel einzuprägen, als einfach
auszumultiplizieren.

Auch bei der Multiplikation zweier komplexer Zahlen kann das Produkt geometrisch
in der Gaußschen Zahlenebene interpretiert werden. Wird das Produkt $z_1 \cdot
z_2$ in der Gaußschen Zahlenebene dargestellt, so müssen die beiden Winkel von
$z_1$ und $z_2$ addiert werden und die Länge ist das Produkt der beiden Längen
von $z_1$ und $z_2$.

```{admonition} Interaktiv: Multiplikation komplexe Zahlen von "Hart und Trocken"
:class: seealso, toggle
Starten Sie das

[Applet Multiplikation komplexe Zahlen](https://www.hartundtrocken.de/my-product/interaktiv-multiplikation-komplexer-zahlen/)

von "Hart und Trocken". Dort können Sie zwei komplexe Zahlen in der Gaußschen
Zahlenebene wählen, indem Sie die beiden blauen Punkte bewegen. Das Produkt dieser
beiden komplexen Zahlen wird orange dargestellt.
```

```{dropdown} Video "Komplexe Zahlen - Gaußsche Zahlenebene Multiplikation" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/EdCqr-TDJgE?si=KomK36ZQY_ARAPLe" title="YouTube video player" frameborder="0" allow="accelerometer;
autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

In diesem Kapitel haben Sie gelernt, wie komplexe Zahlen addiert, subtrahiert
und multipliziert werden. Bei der geometrischen Interpretation der
Multiplikation haben wir gesehen, dass das Produkt mit der Summe der beiden
Winkel zusammenhängt. Das wird uns später zu den beiden alternativen
Darstellungsformen trigonometrische Form und Exponentialform führen. Zunächst
erarbeiten wir uns im nächsten Kapitel die Division zweier komplexer Zahlen und
den Betrag.
