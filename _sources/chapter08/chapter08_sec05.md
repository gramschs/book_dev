# 8.5 Komplexe Zahlen in Exponentialform

Im vorherigen Kapitel haben wir die trigonomtrische Form der komplexen Zahlen
kennengelernt. Ihr Vorteil ist, dass Multiplikation und Division in dieser Form
leicht berechnet und geometrisch interpretiert werden können. Auch die
Exponentialform basiert auf der Darstellung einer komplexen Zahl in
Polarkoordinaten, wie wir in diesem Kapitel lernen werden. Der Vorteil der
Exponentialform ist, dass die Berechnung von Potenzen oder Wurzeln in dieser
Darstellung leicht gelingt.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie kennen die **eulersche Formel**

    $$e^{\varphi \mathrm{i}} = \cos(\varphi) + \sin(\varphi)\,\mathrm{i}$$

  auswendig.
* Sie können eine komplexe Zahl in der **Exponentialform** darstellen.
* Sie können eine komplexe Zahl von der trigonometrischen Form in die
  Exponentialform umrechnen und umgekehrt.
```

## Die eulersche Formel führt zur Exponentialform

Im vorherigen Kapitel haben wir die Darstellung komplexer Zahlen in
trigonometrischer Form kennengelernt. Jede komplexe Zahl $z$ kann durch ihren
Betrag $r$ und ihr Argument $\varphi$ beschrieben werden:

$$z = r \, \big( \cos(\varphi) + \sin(\varphi) \, \mathrm{i}\big).$$

Der Mathematiker [Leonhard Euler](https://de.wikipedia.org/wiki/Leonhard_Euler)
hat herausgefunden, dass für alle Argumente $\varphi$ die sogenannte **eulersche
Formel**

$$e^{\varphi \mathrm{i}} = \cos(\varphi) + \sin(\varphi)\,\mathrm{i}$$

gilt. Mit der eulerschen Formel folgt sofort, dass eine komplexe Zahl in
trigonometrischer Form als

\begin{align*}
z &= r \, \left( \cos(\varphi) + \sin(\varphi) \, \mathrm{i}\right) \\
  &= r \, e^{\varphi  \mathrm{i}} \\
\end{align*}

geschrieben werden kann. Diese Darstellung mit der komplexen Exponentialfunktion
wird **Exponentialform** genannt.

```{admonition} Was ist ... die Exponentialform?
:class: note
Die Exponentialform ist eine alternative Schreibweise einer komplexen Zahl
$z$. In Exponentialform wird eine komplexe Zahl geschrieben als

$$z = r \, e^{\varphi  \mathrm{i}}.$$

Dabei ist $r$ der Betrag der komplexen Zahl (also $r = |z|$) und $\varphi$ ihr 
Argument.
```

## Multiplikation und Division in der Exponentialform

Liegen zwei komplexe Zahlen in der Exponentialform vor, so können für die
Multiplikation und Division die Potenzgesetze genutzt werden. Lautet die erste
komplexe Zahl

$$z_1 = r_1 \, e^{\varphi_1 \mathrm{i}}$$

und die zweite komplexe Zahl

$$z_2 = r_2 \, e^{\varphi_2 \mathrm{i}},$$

dann werden für ihr Produkt die Beträge multipliziert und die Argumente addiert:

$$z_1 \cdot z_2 = r_1 \, r_2 \; e^{(\varphi_1 + \varphi_2) \, \mathrm{i}}.$$

Für die Division gilt dann

$$\frac{z_1}{z_2} = \frac{r_1}{r_2} \; e^{(\varphi_1 - \varphi_2) \, \mathrm{i}}.$$

Die Potenzgesetze werden wir auch für das Potenzieren einer komplexen Zahl
ausnutzen, wie wir im nächsten Kapitel lernen werden. Zunächst halten wir noch
einen häufig benutzten Zusammenhang zwischen der komplexen Exponentialfunktion
und den trigonometrischen Funktionen fest.

## Trigonometrische Funktionen und die komplexe Exponentialfunktion

Mit einem kleinen Rechentrick können wir aus den beiden komplexen Zahlen
$e^{\varphi \, \mathrm{i}}$ und $e^{- \varphi \, \mathrm{i}}$ den Kosinus
erzeugen. Wir addieren die beiden und wechseln in die trigonomterische Form:

$$
e^{\varphi \, \mathrm{i}} + e^{-\varphi \, \mathrm{i}}
= \cos(\varphi) + \sin(\varphi) \, \mathrm{i} + \cos(-\varphi) + \sin(-\varphi) \, \mathrm{i} $$

Da die Kosinus-Funktion gerade ist, gilt aber

$$\cos(-\varphi) = \cos(\varphi).$$

Und da die Sinus-Funktion ungerade ist, gilt

$$\sin(-\varphi) = - \sin(\varphi).$$

Daher wird aus der Summe insgesamt

$$e^{\varphi \, \mathrm{i}} + e^{-\varphi \, \mathrm{i}}  = 2\cdot\cos(\varphi).$$

Das können wir noch auf beiden Seiten durch 2 teilen und erhalten

$$\frac{1}{2} \big( e^{\varphi \, \mathrm{i}} + e^{-\varphi \, \mathrm{i}} \big) =\cos(\varphi).$$

Ein ähnliche Rechnung können wir für

$$e^{\varphi \, \mathrm{i}} - e^{-\varphi \, \mathrm{i}} = 2 \, \mathrm{i} \, \sin(\varphi)$$

durchführen. Insgesamt erhalten wir die beiden folgenden Darstellungen der
Kosinus- und Sinus-Funktion.

```{admonition} Wie können Kosinus/Sinus durch komplexe Exponentialfunktionen dargestellt werden?
:class: note
Der Kosinus und der Sinus lässt sich folgendermaßen durch komplexe Exponentialfunktionen darstellen:
\begin{align*}
\cos(\varphi) &= \frac{1}{2} \big( e^{\varphi \, \mathrm{i}} + e^{-\varphi \, \mathrm{i}} \big), \\
\sin(\varphi) &= \frac{1}{2\mathrm{i}} \big( e^{\varphi \, \mathrm{i}} - e^{-\varphi \, \mathrm{i}} \big).
\end{align*}
```

## Weiteres Lernmaterial

```{dropdown} Video "Eulersche Formel" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/TGJHnQY9cjA"
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Exponentialform" von Daniel Jung
<iframe width="560" height="315" src="https://www.youtube.com/embed/CwxhwTRv65Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope;
picture-in-picture" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

In diesem Kapitel haben wir eine weitere Darstellungsform für komplexe Zahlen
kennengelernt. In dieser Darstellung lassen sich Multiplikation und Division
leicht durchführen, so leicht wie auch in der trigonometrischen Form. Der große
Vorteil der Exponentialform wird erst beim Potenzieren ersichtlich werden, was
wir im nächsten Kapitel behandeln werden.
