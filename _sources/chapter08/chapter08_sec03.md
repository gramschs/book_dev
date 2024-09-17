# 8.3 Betrag, komplexe Konjugation und Division

In dem vorherigen Kapitel haben wir die Addition, Subtraktion und Multiplikation
von komplexen Zahlen kennengelernt. In diesem Kapitel werden wir uns mit der
letzten -- noch fehlenden -- Grundrechenart beschäftigen, nämlich der
**Division**. Dazu führen wir zuerst den **Betrag** einer komplexen Zahl ein und
beschäftigen uns mit der **komplexen Konjugation**.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie können den **Betrag** einer komplexen Zahl berechnen: 

   $$|z|=\sqrt{\text{Re}(z)^2 + \text{Im}(z)^2}.$$

* Sie kennen die **Dreiecksungleichung** für den Betrag komplexer Zahlen: 

   $$|z_1 + z_2| \leq |z_1| + |z_2|.$$
* Sie können die **konjugiert komplexe Zahl** bilden, also eine **komplexe
  Konjugation** durchführen. 
* Sie können die folgenden Rechenregeln für den Betrag anwenden:
    * $|z_1 \cdot z_2| = |z_1| \cdot |z_2|$   
    * $|z| = |\bar{z}|$   
    * $|z| = \sqrt{z \cdot \bar{z}}$
* Sie können zwei komplexe Zahlen in Normalform **dividieren**.
```

## Betrag komplexer Zahlen

Im Gegensatz zu reellen Zahlen sind komplexe Zahlen nicht geordnet. Welche Zahl
ist größer: $-1+3\mathrm{i}$ oder $2-0.5\mathrm{i}$? Auf der Zahlengerade lassen
sich die reellen Zahlen ordnen. $3$ ist größer als $2.7$ und liegt daher weiter
rechts auf der Zahlengeraden. Die geometrische Interpretation der komplexen
Zahlen als Punkte in der Gaußschen Zahlenebene zeigt aber, dass dieses Ordnen in
der Gaußschen Zahlenebene nicht funktioniert. Die Zahl $2-0.5\mathrm{i}$ liegt
zwar weiter rechts als $-1+3\mathrm{i}$. Gleichzeitig liegt aber
$-1+3\mathrm{i}$ höher als $2-0.5\mathrm{i}$. Als Ersatz für eine Ordnung der
komplexen Zahlen dient daher der sogenannte **Betrag** einer komplexen Zahl. Der
Betrag einer komplexen Zahl ist ihr Abstand zum Koordinatenursprung, also zur
Null $0+0\mathrm{i}$.

Verwenden wir den Satz des Pythagoras, können wir den Betrag einer komplexen
Zahl aus ihrem Realteil und Imaginärteil ausrechnen.

```{admonition} Was ist ... der Betrag einer komplexen Zahl?
:class: note
Der Betrag einer komplexen Zahl $z = a + \mathrm{i}$ mit Realteil $a$ und
Imaginärteil $b$ ist

$$|z| = \sqrt{a^2 + b^2}.$$
```

Für den Betrag zweier komplexer Zahlen gilt die sogenannte
**Dreiecksungleichung**:

$$|z_1 + z_2| \leq |z_1| + |z_2|.$$

```{dropdown} Video "Komplexe Zahlen - Betrag" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/09WI_DCFmI0?si=bJrb_PYPcQ3t9cQY" title="YouTube video player" frameborder="0" allow="accelerometer; 
autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

## Komplexe Konjugation

Als nächstes betrachen wir den Prozess der komplexen Konjugation. Soll zu einer
komplexen Zahl die sogenannte **konjugiert komplexe Zahl** berechnet werden,
dann ist damit gemeint, dass das Vorzeichen des Imaginärteils getauscht wird.
Anhand eines Beispiels betrachten wir nun die geometrische Interpretation der
konjugiert komplexen Zahl in der Gaußschen Zahlenebene.

**Beispiel:** Wir betrachten die komplexe Zahl $z = 3 + 2\mathrm{i}$. Tauschen
wir nun das Vorzeichen des Imaginärteils, ergibt sich daraus die konjugiert
komplexe Zahl

$$\bar{z} = 3 \textcolor{red}{-} 2\mathrm{i}.$$

Dabei wird die konjugiert komplexe Zahl durch einen Strich gekennzeichnet. Als
nächstes zeichnen wir $z$ und $\bar{z}$ in der Gaußschen Zahlenebene ein.

<img src="pics/konjugiert_komplexe_zahl_light43.svg"
alt="Komplexe Zahl und ihre konjugiert komplexe Zahl in der Gaußschen Zahlenebene"
class="image43"
width=100%>
<img src="pics/konjugiert_komplexe_zahl_light169.svg"
alt="Komplexe Zahl und ihre konjugiert komplexe Zahl in der Gaußschen Zahlenebene"
class="image169"
width=100%>

Wir können den Prozess des »Vorzeichentauschens«, die sogenannte **komplexe
Konjugation** geometrisch als eine Spiegelung an der Realteil-Achse
interpretieren.

```{admonition} Was ist ... die konjugiert komplexe Zahl?
:class: note
Ist $z = a + b\mathrm{i}$ eine komplexe Zahl, dann wird

$$\bar{z} = a - b\mathrm{i}$$

ihre konjugiert komplexe Zahl genannt. Sie entsteht durch das Tauschen des
Vorzeichens des Imaginärteils. 
```

```{dropdown} Video "Komplexe Zahlen - Konjugiert komplexe Zahl" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/-XZcW-xa35I?si=CB-vYzuUPo-TWTCS" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

## Division komplexer Zahlen

Die Division zweier komplexer Zahlen erfordert einen Trick. Um den Trick zu
erklären, starten wir mit einem Beispiel. Die beiden komplexen Zahlen
$z_1 = 1-3\mathrm{i}$ und $z_2 = 1+2\mathrm{i}$ sollen dividiert werden, also

$$\frac{z_1}{z_2} = \frac{1-3\mathrm{i}}{1+2\mathrm{i}}$$

berechnet werden. Wir nehmen den Nenner $1+2\mathrm{i}$ und tauschen das
Vorzeichen des Imaginärteils aus. Aus Plus machen wir Minus und aus Minus machen
wir Plus und erhalten die folgende konjugiert komplexe Zahl:

$$1+2\mathrm{i} \; \longrightarrow \; 1 \textcolor{red}{-}2\mathrm{i}.$$

Als nächstes erweitern wir den Bruch mit dieser neuen Zahl, rechnen also

$$\frac{1-3\mathrm{i}}{1+2\mathrm{i}} \cdot \frac{1
\textcolor{red}{-}2\mathrm{i}}{1 \textcolor{red}{-}2\mathrm{i}}$$

aus. Beim Ausmultiplizieren des Nenners können wir die [3. binomische
Formel](https://de.wikipedia.org/wiki/Binomische_Formeln) $(a+b)\cdot (a-b) =
a^2 -b^2$ ausnutzen:

$$\frac{(1-3\mathrm{i})}{(1+2\mathrm{i})} \cdot \frac{(1
\textcolor{red}{-}2\mathrm{i})}{(1 \textcolor{red}{-}2\mathrm{i})} =
\frac{1-2\mathrm{i}-3\mathrm{i}+6\mathrm{i}^2}{1^2 - 4\mathrm{i}^2}
.$$

Da ja $\mathrm{i}^2 = -1$ gilt, vereinfachen sich die Terme zu

$$\frac{1-2\mathrm{i}-3\mathrm{i}+6\mathrm{i}^2}{1^2 - 4\mathrm{i}^2}
= \frac{-5 -5\mathrm{i}}{5}.$$

Daher gilt also insgesamt

$$\frac{z_1}{z_2} = \frac{1-3\mathrm{i}}{1+2\mathrm{i}} = \frac{-5
-5\mathrm{i}}{5} = -1 -\mathrm{i}.$$

Um zwei komplexe Zahlen in Normalform zu dividieren, gehen wir also in drei
Schritten vor:

1. Bei der komplexen Zahl im Nenner wird das Vorzeichen des Imaginärteils
   getauscht, also die konjugiert komplexe Zahl des Nenners gebildet.
2. Danach wird der Bruch mit der kongugiert komplexen Zahl erweitert.
3. Zuletzt werden alle Terme durch Ausmultiplizieren vereinfacht. Dabei werden
   die 3. binomische Formel und $\mathrm{i}^2=-1$ ausgenutzt, bis das Ergebnis
   in Normalform dasteht.  

Der Vollständigkeit halber notieren wir noch die mathematische Formel zur
Berechnung eines Quotienten von komplexen Zahlen im Allgemeinen. Wenn $z_1 =
a_1 + b_1 \cdot \mathrm{i}$ und $z_2 = a_2 + b_2 \cdot \mathrm{i}$ komplexe Zahlen
sind, dann ist ihr Quotient

$$\frac{z_1}{z_2} = \frac{a_1 + b_1 \cdot \mathrm{i}}{a_2 + b_2 \cdot
\mathrm{i}} = \frac{a_1a_2 + b_1 b_2}{a_2^2 + b_2^2} + \frac{a_2 b_1 - a_1
b_2}{a_2^2 + b_2^2} \mathrm{i}.$$

Es ist wenig sinnvoll, diese Formel auswendig zu lernen. Eine bessere Strategie
ist, sich zu merken, dass mit der konjugiert komplexen Zahl erweitert wird. Auch
die Division zweier komplexer Zahlen kann geometrisch in der Gaußschen
Zahlenebene interpretiert werden. Probieren Sie dazu das folgende Applet aus.

```{admonition} Interaktiv: Division komplexer Zahlen von "Hart und Trocken"
:class: seealso, toggle
Starten Sie das

[Applet "Division komplexer
Zahlen"](https://www.hartundtrocken.de/my-product/interaktiv-division-komplexer-zahlen/)

von "Hart und Trocken". Dort können Sie zwei komplexe Zahlen in der Gaußschen
Zahlenebene wählen, indem Sie die beiden blauen Punkte bewegen. Der Quotient dieser
beiden komplexen Zahlen wird orange dargestellt.
```

```{dropdown} Video "Komplexe Zahlen - Kehrwert einer komplexen Zahl" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/Rxq-4o1eFNA?si=yUlycavP-smHAGAP" title="YouTube video player" frameborder="0" allow="accelerometer;
autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

```{dropdown} Video "Komplexe Zahlen | Division" von Lernkompass
<iframe width="560" height="315" src="https://www.youtube.com/embed/J8btoGTJW-k?si=c057mP3tROAx6hHs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

## Weiteres Lernmaterial

```{dropdown} Video "Komplexe Mengen grafisch darstellen" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/M4KewnSNyC4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

In diesem Kapitel haben Sie gelernt, wie komplexe Zahlen dividiert werden. Dazu
wurden die Begriffe Betrag und komplexe Konjugation eingeführt. Tatsächlich ist
es bei der Multiplikation und der Division häufig geschickter, von der
Darstellung einer komplexen Zahl in Normalform zu der sogenannten
trigonometrischen Form oder Exponentialform überzugehen. Letzteres wird uns auch
das Potenzieren und Wurzelziehen ermöglichen. Daher behandeln wir im nächsten
Kapitel zunächst die trigonometrische Form der komplexen Zahlen.
