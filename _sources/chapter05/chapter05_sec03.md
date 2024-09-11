# 5.3 Lineare Gleichungssysteme

Lineare Gleichungssysteme kommen in vielen Anwendungen vor. Ein typisches
Anwendungsszenario sind Kräfteberechnungen in der Technischen Mechanik. Wir
werden im nächsten Kapitel lineare Gleichungssysteme benötigen, um die Lage von
Geraden und Ebenen zu untersuchen. Daher beschäftigen wir uns in diesem Kapitel
mit linearen Gleichungssytemen, die aus drei Gleichungen mit drei Unbekannten
bestehen.

## Lernziele

```{admonition} Lernziele
:class: goals
- Sie wissen, dass ein lineares Gleichungssystem eine **eindeutige Lösung**,
  **unendlich viele Lösungen** oder **keine Lösung** haben kann.
- Sie können mit dem **Gauß-Algorithmus** für alle drei Fälle die Lösung(en)
  berechnen.
```

## Gauß-Algorithmus

Für zwei Gleichungen mit zwei Unbekannten gibt es mehrere Verfahren, das
Gleichungssytem zu lösen. In der Schule lernt man beispielsweise das
Additionsverfahren oder das Gleichsetzungsverfahren. Bei drei Gleichungen mit
drei Unbekannten oder noch größeren Gleichungssystemen ist es sinnvoll, eine
festgelegte Strategie zu verfolgen, da man sonst leicht den Überblick verliert.
Ein bewährtes Verfahren zum Lösen von linearen Gleichungssytemen mit drei und
mehr Gleichungen ist der **Gauß-Algorithmus**.

Beim Gauß-Algorithmus wird das lineare Gleichungssytem zunächst in eine
**Dreiecksform** gebracht. Anstatt Dreiecksform wird auch der Begriff
**Zeilen-Stufenform** verwendet. Danach werden die Unbekannten durch
**Rückwärtseinsetzen** berechnet. Im Folgenden wird der Gauß-Algorithmus an
einem Beispiel demonstriert.

Gegeben ist das folgende lineare Gleichungssystem:

\begin{align*}
3x_1  - 4x_2 - 4x_3 &= -4  \\
6x_1  - 6x_2 - 7x_3 &= -11 \\
-3x_1 + 6x_2 + 7x_3 &= 11 \\
\end{align*}

Wir wollen das lineare Gleichungssystem in die Dreiecksform bringen. Um einen
besseren Überblick zu behalten, welche Umformungen dabei vorgenommen werden,
nummerieren wir die Gleichungen mit (Z1), (Z2) und (Z3) für Zeile 1, Zeile 2 und
Zeile 3.

\begin{alignat*}{2}
3x_1 - 4x_2 - 4x_3   &= -4  & &\quad (\text{Z1}) &\\
6x_1 - 6x_2 - 7x_3   &= -11 & &\quad (\text{Z2}) &\\
-3x_1 + 6x_2 + 7x_3  &= 11 & &\quad (\text{Z3}) &\\
\end{alignat*}

Jetzt formen wir die zweite Gleichung um. Ziel der Umformung ist es, geschickt
Vielfache der ersten Gleichung zu Vielfachen der zweiten Gleichung zu addieren,
so dass de Term $6x_1$ zu Null wird. Dazu multiplizieren wir die 1. Zeile mit 2
und subtrahieren dann die 2. Zeile. Diesen Schritt führen wir in einer
Zwischenrechnung aus:

$$\begin{array}{crrrrr}
2\cdot (\text{Z1})              \quad & 6x_1  & -8x_2 & - 8x_3 &=& -8 \\
-(\text{Z2})                    \quad & -6x_1 & +6x_2 & + 7x_3 &=& 11 \\ \hline
2\cdot (\text{Z1})-(\text{Z2})  \quad &  & -2x_2 & - x_3  &=& 3\\
\end{array}$$

Jetzt wird die dritte Gleichung umgeformt. Diesmal ist das Ziel, $-3x_1$ auf
Null zu bringen. Dazu brauchen wir nur 1. Zeile und 3. Zeile zu addieren. Die
Zwischenrechnung lautet wie folgt:

$$\begin{array}{crrrrr}
(\text{Z1})             \quad &  3x_1 & -4x_2 & -4x_3 &=& -4 \\
+(\text{Z3})            \quad & -3x_1 & +6x_2 & +7x_3 &=& 11 \\ \hline
(\text{Z1})+(\text{Z3}) \quad &       &  2x_2 & +3x_3 &=& 7 \\
\end{array}$$

Nachdem wir diese Zwischenrechnungen durchgeführt haben, können wir die alten
Gleichungen (Z2) und (Z3) durch die neuen Gleichungen ersetzen. Auf der linken
Seite schreiben wir uns zur Erinnerung auf, welche Umformungen durchgeführt
wurden. Auf der rechten Seite nummerieren wir neu durch.

\begin{alignat*}{2}
    && \quad 3x_1 - 4x_2 - 4x_3 &=-4 &&\quad (\text{Z1})\\
\textcolor{lightgray}{2\cdot (\text{Z1})-(\text{Z2})}  
    && \quad  -2x_2 -x_3        &=3  &&\quad (\text{Z2})\\
\textcolor{lightgray}{(\text{Z1})+(\text{Z3})}
    && \quad  2x_2 + 3x_3       &=7 &&\quad (\text{Z3})\\
\end{alignat*}

Der letzte Schritt zur Dreiecksform ist, die neue 3. Gleichung zo umzuformen,
dass der Term $2x_2$ verschwindet. Dazu brauchen wir aber nur die neue 2.
Gleichung und die neue 3. Gleichung addieren. Wir lassen diesmal die
ausführliche Zwischenrechnung weg und schreiben gleich das neue Gleichungssystem
auf:

\begin{alignat*}{2}
    && \quad 3x_1 - 4x_2 - 4x_3 &=-4 &&\quad (\text{Z1})\\
    && \quad  -2x_2 -x_3        &=3  &&\quad (\text{Z2})\\
\textcolor{lightgray}{(\text{Z2})+(\text{Z3})}
    && \quad   2x_3             &=10 &&\quad (\text{Z3})\\
\end{alignat*}

Damit liegt das lineare Gleichungssystem in Dreiecksform vor. Nun lösen wir das
Gleichungssystem durch **Rückwärtseinsetzen**. Wir nehmen uns die unterste
Gleichung. Sie lautet

$$(\text{Z3}) \quad 2x_3 = 10.$$

Daraus folgt sofort $x_3 = 5$. Nun wird $x_3 = 5$ in Gleichung $(\text{Z2})$
eingesetzt und dann nach $x_2$ aufgelöst:

$$(\text{Z2}) \quad -2x_2 - 5 = 3 \quad \Rightarrow \quad x_2 = -4.$$

Nun werden $x_3 = 5$ und $x_2 = -4$ in Gleichung $(\text{Z1})$ eingesetzt und
dann nach $x_1$ aufgelöst:

$$(\text{Z1}) \quad 3x_1 - 4\cdot(-4) - 4\cdot 5 = -4 \quad \Rightarrow \quad x_1
= 0.$$

Die Lösung des linearen Gleichungssystems ist eindeutig, die Lösungsmenge ist

$$\mathbb{L} = \{(0 \vert -4 \vert 5)\}.$$

```{admonition} Übung
:class: miniexercise
Lösen Sie auf der Internetseite
[https://mathebattle.de/edu_randomtasks/training_show/39](https://mathebattle.de/edu_randomtasks/training_show/39) solange lineare Gleichungssysteme mit dem Gauß-Verfahren, bis Sie dreimal
hintereinander eine Aufgabe korrekt gelöst haben.
```

## Unendliche viele Lösungen

Auch wenn die Gleichungen nicht zueinander passen, liefert der Gauß-Algorithmus
eine passende Berechnungsvorschrift. In dem folgenden Beispiel ist eine
Gleichung überflüssig. Das lineare Gleichungssytem hat unendlich viele Lösungen.
Wir schauen uns an, wie dieser Fall mit dme Gauß-Algorithmus detektiert wird und
wie die unendlich vielen Lösungen berechnet und beschrieben werden.

\begin{alignat*}{2}
x_1 + 9x_2 - 8x_3  &= 0  & &\quad (\text{Z1}) &\\
-2x_1 + 9x_2 + 7x_3   &= -27 & &\quad (\text{Z2}) &\\
3x_1 \phantom{+ 9x_2} - 15x_3  &= 27 & &\quad (\text{Z3}) &\\
\end{alignat*}

Eliminieren der ersten Terme der 2. und 3. Gleichung liefert:

\begin{alignat*}{2}
    && \quad x_1 + 9x_2 - 8x_3 &= 0 &&\quad (\text{Z1})\\
\textcolor{lightgray}{2\cdot (\text{Z1})+(\text{Z2})}  
    && \quad  27x_2 -9x_3        &=-27  &&\quad (\text{Z2})\\
\textcolor{lightgray}{3\cdot(\text{Z1})-(\text{Z3})}
    && \quad  27x_2 -9x_3       &=-27 &&\quad (\text{Z3})\\
\end{alignat*}

Eliminieren des zweiten Terms der 3. Gleichung ergibt:

\begin{alignat*}{2}
    && \quad x_1 + 9x_2 - 8x_3 &= 0 &&\quad (\text{Z1})\\
    && \quad  27x_2 -9x_3        &=-27  &&\quad (\text{Z2})\\
\textcolor{lightgray}{3\cdot(\text{Z1})-(\text{Z3})}
    && \quad  0     &=0 &&\quad (\text{Z3})\\
\end{alignat*}

Diesmal liegt kein Widerspruch vor. Leider haben wir zwar mit der 3. Zeile $0=0$
eine wahre Aussage, aber diese Aussage hat keinen Informationsgehalt für unser
Gleichungssystem. Es gibt nur noch zwei Gleichungen mit Informationen darüber,
wie die drei Variablen $x_1$, $x_2$ und $x_3$ zusammenhängen. Ein solches
Gleichungssystem, bei dem es weniger Gleichungen als Unbekannte gibt, wird
**unterbestimmtes Gleichungssytem** genannt.

Da es keinen Konflikt in 3. Gleichung, wenn wir annehmen, dass $x_3$ eine
beliebige Zahl ist, es gibt also unendliche viele Lösungen. Um formal auch
kenntlich zu machen, dass jede bleibige Zahl für $x_3$ verwendet werden darf,
führen wir den sogenannten **Parameter** $t$ ein und setzen die gescuhte Lösung
auf $t$, also

$$(\text{Z3}) \quad x_3 = t.$$

Diese »Lösung« setzen wir dann in die 2. Gleichung ein und lösen nach $x_2$ auf:

$$(\text{Z2})\quad 27x_2 -9t = -27 \quad\Rightarrow\quad x_2 = -1 + \frac{1}{3}t.$$

Nun setzen wir $x_3 = t$ und $x_2 = -1 + \frac{1}{3}t$ in die 1. Gleichung ein
und lösen nach $x_1$ auf:

$$(\text{Z1})\quad x_1 + 9\cdot (-1 + \frac{1}{3}t)-8t = 0 \quad\Rightarrow\quad
x_1 = 9 + 5t.$$

Die Lösungsmenge ist also

$$\mathbb{L} = \left\{\left( 9+5t \Big| -1 + \frac{1}{3}t \Big| t \right)\right\}.$$

Das kann mann auch in Vektorschreibweise notieren:

$$\vec{x}=\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} =
\begin{pmatrix} 9+5t \\ -1 + \frac{1}{3}t\\ 0 + t \end{pmatrix} =
\begin{pmatrix} 9 \\ -1 \\ 0 \end{pmatrix} + t\cdot
\begin{pmatrix} 5 \\ \frac{1}{3}\\ 1 \end{pmatrix}.$$

Dabei haben wir in der dritten Komponente den Trick $t = 0 + t$ verwendet.

Es gibt also unendliche viele Lösungen.

```{admonition} Übung
:class: miniexercise
Lösen Sie auf der Internetseite
[https://mathebattle.de/edu_randomtasks/training_show/457](https://mathebattle.de/edu_randomtasks/training_show/457) solange lineare Gleichungssysteme mit dem Gauß-Verfahren, bis Sie dreimal
hintereinander eine Aufgabe korrekt gelöst haben.
```

## Keine Lösung

Ein lineares Gleichungssytem kann auch keine Lösung haben, wenn Gleichungen
zueinander im Konflikt stehen. Der Gauß-Algorithmus zeigt uns, ob ein solcher
Fall vorliegt. Wir nehmen das Beispiel

\begin{alignat*}{2}
-2x_1 + 9x_2 - 10x_3  &= -68  & &\quad (\text{Z1}) &\\
-8x_1 + 2x_2 + 3x_3   &= 204 & &\quad (\text{Z2}) &\\
14x_1 + 5x_2 - 16x_3  &= -475 & &\quad (\text{Z3}) &\\
\end{alignat*}

Eliminieren der ersten Terme der 2. und 3. Gleichung liefert:

\begin{alignat*}{2}
    && \quad -2x_1 + 9x_2 - 10x_3 &=-68 &&\quad (\text{Z1})\\
\textcolor{lightgray}{4\cdot (\text{Z1})-(\text{Z2})}  
    && \quad  34x_2 -43x_3        &=-476  &&\quad (\text{Z2})\\
\textcolor{lightgray}{7\cdot(\text{Z1})+(\text{Z3})}
    && \quad  68x_2 -86 x_3       &=-951 &&\quad (\text{Z3})\\
\end{alignat*}

Eliminieren des zweiten Terms der 3. Gleichung ergibt:

\begin{alignat*}{2}
    && \quad -2x_1 + 9x_2 - 10x_3 &=-68 &&\quad (\text{Z1})\\
    && \quad  34x_2 -43x_3        &=-476  &&\quad (\text{Z2})\\
\textcolor{lightgray}{2\cdot(\text{Z2})-(\text{Z3})}
    && \quad 0   &=-1 &&\quad (\text{Z3})\\
\end{alignat*}

In der 3. Gleichung liegt ein Widerspruch vor. Die Aussage $0=-1$ ist falsch.
Damit kann das lineare Gleichungssystem keine Lösung haben. Wir schreiben

$$\mathbb{L} = \{\,\}.$$

für die Lösungsmenge die leere Menge hin.

```{admonition} Übung
:class: miniexercise
Lösen Sie auf der Internetseite
[https://mathebattle.de/edu_randomtasks/training_show/863](https://mathebattle.de/edu_randomtasks/training_show/863) solange lineare Gleichungssysteme mit dem Gauß-Verfahren, bis Sie dreimal
hintereinander eine Aufgabe korrekt gelöst haben.
```

In dem folgenden Video werden alle drei Möglichkeiten noch einmal ausführlich
vorgerechnet.

```{dropdown} Video "Gauß Algorithmus – Lineare Gleichungssysteme lösen" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/aosbq7Ci7Ec?si=rMF-Fqs1W_xRivC3" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay;
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

Im nächsten Kapitel werden wir lineare Gleichungssyteme aufstellen, um zu
untersuchen, ob sich Geraden und Ebenen schneiden. Mit Hilfe des
Gauß-Algorithmus werden wir Schnittpunkte und Schnittgeraden berechnen.
