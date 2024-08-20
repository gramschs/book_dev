# 8.6 Potenzen und Wurzeln komplexer Zahlen

Auf die komplexen Zahlen stießen wir, indem wir versuchten, die Gleichung $z^2 =
-1$ zu lösen. In diesem Kapitel beschäftigen wir uns nun mit dem Potenzieren und
Wurzelziehen für komplexe Zahlen.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie können eine komplexe Zahl potenzieren.
* Sie können aus einer komplexen Zahl die Wurzel ziehen.
```

## Potenzen von komplexen Zahlen

Die Potenz einer komplexen Zahl ist – genau wie bei den reellen Zahlen – eine
Abkürzung für das wiederholte Multiplizieren einer Zahl mit sich selbst.

\begin{align*}
z^2 &= z\cdot z \\
z^3 &= z \cdot z \cdot z \\
z^4 &= z \cdot z \cdot z \cdot z \\
z^5 &= z \cdot z \cdot z \cdot z \cdot z\\
\vdots
\end{align*}

Die Zahl $z$ heißt Basis und die Anzahl, wie oft die Basis mit sich selbst
multipliziert wird, heißt Exponent oder Hochzahl. Es gibt auch negative Potenzen:

\begin{align*}
z^{-2} &= \frac{1}{z\cdot z} \\
z^{-3} &= \frac{1}{z \cdot z \cdot z} \\
z^{-4} &= \frac{1}{z \cdot z \cdot z \cdot z} \\
z^{-5} &= \frac{1}{z \cdot z \cdot z \cdot z \cdot z}\\
\vdots
\end{align*}

Wenn nun konkret eine Potenz einer komplexen Zahl ausgerechnet werden soll, ist
die Exponentialform am besten geeignet, wie das folgende Beispiel zeigt. Wir
möchten von der komplexen Zahl $z = 3e^{\frac{\pi}{4}\mathrm{i}}$ die Potenzen
bis 4 bilden.

Für die 2. Potenz erhalten wir zufälligerweise eine rein imaginäre Zahl, wie die
folgende Rechnung zeigt:

\begin{align*}
z^2
&= \left( 3e^{\frac{\pi}{4}\mathrm{i}} \right) \cdot \left( 3e^{\frac{\pi}{4}\mathrm{i}} \right)\\
&= 3^2 \cdot e^{\left(\frac{\pi}{4}+\frac{\pi}{4}\right)\mathrm{i}} \\
&= 9 \, e^{\frac{\pi}{2} \mathrm{i}} \\
&= 9\mathrm{i}.
\end{align*}

Für die 3. Potenz erhalten wir

\begin{align*}
z^3
&= \left( 3e^{\frac{\pi}{4}\mathrm{i}} \right) \cdot \left( 3e^{\frac{\pi}{4}\mathrm{i}} \right)\cdot \left( 3e^{\frac{\pi}{4}\mathrm{i}} \right)\\
&= 3^3 \cdot e^{\left(\frac{\pi}{4}+\frac{\pi}{4}+\frac{\pi}{4}\right)\mathrm{i}} \\
&= 27 \, e^{\frac{3}{4}\pi \mathrm{i}} \\
&\approx -19.0919 + 19.0919 \, \mathrm{i}.
\end{align*}

Und die 4. Potenz ist zufälligerweise rein reell:

\begin{align*}
z^4
&= \left( 3e^{\frac{\pi}{4}\mathrm{i}} \right) \cdot \left( 3e^{\frac{\pi}{4}\mathrm{i}} \right) \cdot \left( 3e^{\frac{\pi}{4}\mathrm{i}} \right) \cdot \left( 3e^{\frac{\pi}{4}\mathrm{i}} \right)\\
&= 3^4 \cdot e^{\left(\frac{\pi}{4}+\frac{\pi}{4}+\frac{\pi}{4}+\frac{\pi}{4}\right)\mathrm{i}} \\
&= 81 \cdot e^{\pi \mathrm{i}} \\
&= 81 \cdot (-1) \\
&= -81.
\end{align*}

Zusammengefasst gilt für das Potenzieren von komplexen Zahlen die folgende
Rechenregel.

```{admonition} Wie wird eine komplexe Zahl potenziert?
:class: note
Für jeden ganzzahligen Exponenten $n$ wird die n-te Potenz einer komplexen Zahl
$z = r e^{\varphi\,\mathrm{i}}$ berechnet, indem der Betrag $r$ mit $n$ potenziert
wird und das Argument $\varphi$ mit $n$ multipliziert wird:

$$z^n = \big(r e^{\varphi\,\mathrm{i}}\big)^n = r^n e^{n\, \varphi \, \mathrm{i}}.$$
```

Wie geht man vor, wenn die komplexe Zahl in Normalform oder trigonometrischer
Form vorliegt? In Normalform können die Klammern einfach ausmultipliziert
werden. Bei höhereren Potenzen ist es nur etwas schwierig, den Überblick über
die einzelnen Terme zu behalten. Für die trigonometrische Form gibt es den [Satz
von de Moivre](https://de.wikipedia.org/wiki/Moivrescher_Satz), auf die wir hier
aber nicht weiter eingehen.

```{dropdown} Video "Komplexe Zahlen potenzieren" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/G_FRNyHpzrk" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Potenzieren von komplexen Zahlen" von Hart und Trocken
<iframe width="560" height="315" src="https://www.youtube.com/embed/F2EjFIlOQLs?si=Fa1xw6X6pCYKpITg" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{admonition} interaktives Applet "Potenzen von komplexen Zahlen" von Hart und Trocken
:class: seealso
https://www.hartundtrocken.de/my-product/interaktiv-potenzen-komplexer-zahlen/
```

## Wurzelziehen von komplexen Zahlen

Von den Potenzen ist der Schritt zu den Wurzeln recht kurz. Sie treten auf, wenn
wir beispielsweise die quadratische Gleichung

$$z^2 = 3 + 4\, \mathrm{i}$$

lösen wollen. Bei reellen quadratischen Gleichungen kann es keine, eine oder
zwei Lösungen geben. Eine komplexe quadratische Gleichung hat immer zwei
Lösungen. Zuerst wandeln wir die komplexe Zahl von der Normalform in die
Exponentialform um:

$$z^2 = 3 + 4\mathrm{i} = 5 \, e^{53.130^{\circ}\mathrm{i}}.$$

Bei der Berechnung der 2. Potenz müssen wir den Betrag quadrieren und das
Argument mit 2 multiplizieren, um auf $5 \, e^{53.13^{\circ}\mathrm{i}}$ zu
kommen. Diesen Prozess kehren wir jetzt um. Wir ziehen aus dem Betrag 5 die
Wurzel und teilen das Argument $53.13^{\circ}$ durch 2:

$$z_1 = \sqrt{5} \, e^{\frac{53.13^{\circ}}{2}\mathrm{i}}.$$

Zur Kontrolle berechnen wir $z_1^2$:

\begin{align*}
z_1^2 &= \sqrt{5} \, e^{\frac{53.13^{\circ}}{2}\mathrm{i}} \cdot \sqrt{5} \, e^{\frac{53.13^{\circ}}{2}\mathrm{i}}\\
&= \sqrt{5}\cdot\sqrt{5}\, e^{\left( \frac{53.13^{\circ}}{2} +  \frac{53.13^{\circ}}{2} \right) \mathrm{i}} \\
&= 5 e^{53.13^{\circ}\mathrm{i}}.
\end{align*}

Und die zweite Lösung? Wenn wir auf das Argument der ersten Lösung $\varphi_1 =
\frac{53.13^{\circ}}{2} = 26.565^{\circ}$ den Winkel $180^{\circ}$ addieren,
erhalten wir die zweite Lösung. Testen wir, ob das stimmt.

\begin{align*}
z_2^2 &= \sqrt{5} \, e^{206.565^{\circ}\mathrm{i}} \cdot \sqrt{5} \,  e^{206.565^{\circ}\mathrm{i}}\\
&= \sqrt{5}\cdot\sqrt{5}\, e^{\left( 206.565^{\circ} +  206.565^{\circ} \right) \mathrm{i}} \\
&= 5 e^{413.13^{\circ}\mathrm{i}}.
\end{align*}

Zunächst sieht es nicht so aus, als ob $z_2 = 5 \, e^{53.130^{\circ}\mathrm{i}}$
gelte. Aber das Argument $413.13^{\circ}$ ist ja größer als $360^{\circ}$.
Ziehen wir die $360^{\circ}$ ab, um ein Argument zwischen $0^{\circ}$ und
$360^{\circ}$ zu erhalten, landen wir wieder bei

$$z_2^{2} =  5 e^{53.13^{\circ}\mathrm{i}} = 3 + 4\mathrm{i}.$$

Also ist auch $z_2$ eine Lösung der quadratischen Gleichung.

Dieses Vorgehen zur Berechnung der Wurzeln behalten wir bei. Wenn die fünfte
Wurzel gezogen werden soll, ziehen wir zuerst die 5.-te Wurzel aus dem Betrag
und teilen das Argument durch 5. Die anderen vier Wurzeln berechnen wir dann,
indem wir $360^{\circ}$ durch 5 teilen und jetzt viermal hintereinander auf das
Argument der ersten berechneten Wurzel $72^{\circ}$ addieren.

Die n-ten Wurzeln einer komplexen Zahl $r\, e^{\varphi \, \mathrm{i}}$ lassen
sich folgendermaßen berechnen. Die erste n-te Wurzel erhalten wir, indem wir die
n-te Wurzel des Betrages $r$ berechnen und das Argument $\varphi$ durch $n$
teilen:

$$z_1 = \sqrt[n]{r} e^{\frac{\varphi}{n}\, \mathrm{i}}.$$

Für die weiteren n-ten Wurzeln wird $\Delta\varphi = \frac{360^{\circ}}{n}$ zu
dem Argument der ersten Lösung $\frac{\varphi}{n}$ addiert. Das Argument der 2.
Lösung ist also

$$\varphi_2 =  \frac{\varphi}{n} + \Delta\varphi$$

Wenn nach der 2. Wurzel gefragt ist, haben wir $\Delta\varphi = 180^{\circ}$
addiert und sind wir hier fertig. Wenn jedoch die 3. Wurzel berechnet werden
sollte, war $\Delta\varphi = 120^{\circ}$ und wir müssen noch die 3. Wurzel
berechnen. Dazu addieren wir noch einmal $\Delta\varphi$. Das Argument der
dritten Lösung ist also

$$\varphi_3 =  \frac{\varphi}{n} + 2\cdot \Delta\varphi.$$

Sollte nach der 4. Wurzel gefragt worden sein, müssen wir $\Delta\varphi =
90^{\circ}$ addieren und erneut weitermachen:

$$\varphi_4 =  \frac{\varphi}{n} + 3\cdot \Delta\varphi.$$

Und dieses Schema setzt sich so fort. Übrigens, falls der Winkel nicht im
Gradmaß, sondern im Bogenmaß angegeben ist, wird $\Delta\varphi =
\frac{2\pi}{n}$ addiert.

```{admonition} Wie werden die n-ten Wurzeln einer komplexen Zahl berechnet?
:class: note
Die n-ten Wurzeln einer komplexen Zahl $z = r\, e^{\varphi\, \mathrm{i}}$ lauten

$$z_k = \sqrt[n]{r} \, e^{\left(\frac{\varphi}{n}+(k-1)\cdot\Delta\varphi\right)\mathrm{i}}$$

mit $\Delta\varphi=\frac{360^{\circ}}{n} = \frac{2\pi}{n}$ und $k = 1, \ldots,
n$.
```

```{dropdown} Video "Wurzeln von komplexen Zahlen: Einführung" von Hart und Trocken
<iframe width="546" height="307" src="https://www.youtube.com/embed/fZ1poJc_s7I" 
title="Wurzeln von komplexen Zahlen: Eine Einführung" frameborder="0" allow="accelerometer; 
autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Wurzeln von komplexen Zahlen: Berechnung und Darstellung" von Hart und Trocken
<iframe width="546" height="307" src="https://www.youtube.com/embed/aUZn57OsIeU" 
title="Wurzeln von komplexen Zahlen: Berechnung und Darstellung" frameborder="0" 
allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; 
web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Komplexe Zahlen radizieren" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/BKdqTn2iO4s" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{admonition} interaktives Applet "Wurzeln von komplexen Zahlen" von Hart und Trocken
:class: seealso
https://www.hartundtrocken.de/my-product/interaktiv-wurzeln-komplexer-zahlen/
```

## Zusammenfassung und Ausblick

Mit dem Potenzieren und dem Wurzelziehen ist unser Ausflug in die komplexen
Zahlen hier erst einmal beendet. Im nächsten Kapitel steigen wir mit dem Thema
»Funktionen« in die eindimensionale Analysis ein.
