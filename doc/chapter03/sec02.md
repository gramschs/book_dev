# 3.2 Vektoren und Vektorräume

Im letzten Kapitel haben wir n-Tupel kennengelernt. Je nachdem für welche
Anwendung sie eingesetzt werden, ist es sinnvoll, damit rechnen zu können.
n-Tupels zusammen mit bestimmten Rechenoperationen führen zu dem Begriff des
Vektorraumes, den wir in diesem Kapitel behandeln werden.

## Lernziele Vektoren

```{admonition} Lernziele 
:class: goals
* Sie wissen, wie der **reelle Standardvektorraum** definiert ist, d.h. Sie können die
  * **Vektoraddition** und
  * **Skalarmultiplikation**
  für n-Tupels anwenden.
* Sie wissen, dass ein Element eines Vektorraumes **Vektor** genannt wird.
* Sie wissen, wie ein allgemeiner, reeller **Vektorraum** definiert ist. Insbesondere können Sie die vier Eigenschaften der Vektoraddition und die vier Eigenschaften der Skalarmultiplikation nachprüfen.
* **Eigenschaften der Vektoraddition**:
  * Assoziativgesetz: $u\oplus(v\oplus w) = (u\oplus v)\oplus w$
  * Existenz eines neutralen Elements $0\in V$ mit $v\oplus 0 = 0\oplus v = v$
  * Existenz eines zu $v\in V$ inversen Elements $-v\in V$ mit $v\oplus (-v)= (-v)\oplus v = 0$
  * Kommutativgesetz: $v\oplus u = u \oplus v$
* **Eigenschaften der Skalarmultiplikation**:
  * Vektorielles Distributivgesetz: $s\odot(u\oplus v) = (s\odot u) \oplus (s\odot v)$
  * Skalares Distributivgesetz: $(s+t)\odot v = (s\odot v) \oplus (t\odot v)$
  * Assoziativgesetz für Skalare: $(s\cdot t)\odot v = s\odot (t \odot v)$
  * Existenz eines neutralen Elements: $1\odot v = v$
```


## Rechnen mit n-Tupeln

Im vorherigen Kapitel haben wir die n-Tupel kennengelernt, eine Liste von $n$
mathematischen Objekten, bei denen die Reihenfolge festgelegt ist. Eine
Anwendung von n-Tupeln in der Praxis könnte die Erfassung der Arbeitsstunden pro
Woche sein. Das erste Element des Tupels steht für die Arbeitsstunden am Montag,
das zweite für den Dienstag, das dritte für den Mittwoch, das vierte für den
Donnerstag und der letzte Eintrag erfasst die Arbeitsstunden am Freitag.
Beispielsweise könnte die Erfassung der Arbeitsstunden für die erste Woche im
Januar $(8, 8, 6, 8, 10)$ sein. Wir bezeichnen dieses 5-Tupel mit $w_1$ für
erste Woche, also

$$w_1 = (8, 8, 6, 8, 10).$$

In der zweiten, dritten und vierten Woche des Januars könnte eine Person
folgende Arbeitsstunden geleistet haben:

\begin{align*}
w_2 &= (7, 7, 10, 8, 8) \\
w_3 &= (8, 8, 8, 8, 8) \\
w_4 &= (7, 9, 8, 7, 9) \\
\end{align*}

Sollen nun die Arbeitsstunden im Januar ausgewertet werden, können wir
beispielsweise fragen, wie viele Stunden insgesamt in den beiden ersten Wochen
gearbeitet wurden. Dazu müssen wir jeden Eintrag (Wochentag) von $w_1$ mit jedem
Eintrag (Wochentag) von $w_2$ addieren:

$$w_1 \oplus w_2 = (8, 8, 6, 8, 10) \oplus (7, 7, 10, 8, 8) = (15, 15, 16, 16, 18).$$

Um deutlich zu machen, dass die »Addition« der beiden 5-Tupel etwas Neues ist,
haben wir das Symbol $\oplus$ verwendet. Addieren wir die ersten vier Wochen im
Januar komponentenweise (also Wochentag für Wochentag), dann erhalten wir

$$\text{Januar} = w_1 \oplus w_2 \oplus w_3 \oplus w_4 = (30, 32, 32, 31, 35).$$

Im Januar hat diese Person mehr Stunden am Freitag gearbeitet als an den anderen
Tagen. Offensichtlich arbeitet diese Personen jede Woche unterschiedlich. Wenn
wir nun analysieren wollen, wie eine durchschnittliche Woche im Januar aussieht,
können wir jede Komponente durch 4 teilen (bzw. mit $\frac{1}{4}$
multiplizieren.

$$\text{Durchschnitt Januar} = \frac{1}{4} \odot (30, 32, 32, 31, 35) = (7.5, 8, 8,
7.75, 8.75).$$

Das Rechnen mit n-Tupeln wollen wir nun formalisieren.


## Der reelle Standardvektorraum

Zunächst formalisieren wir die Schreibweise der Menge aller n-Tupel, indem wir
das kartesische Produkt einführen. Ist $n$ eine natürliche Zahl und $\mathbb{R}$
die Menge der reellen Zahlen, dann ist das n-fache kartesische Produkt

$$\mathbb{R}^{n} = \{(x_1, x_2, \ldots, x_n) \;|\; x_1, x_2, \dots,x_n \in
\mathbb{R}\}$$

die Menge aller n-Tupel $(x_1, x_2, \ldots, x_n)$ mit reellen Zahlen als
Komponenten. Für diese Tupel definieren wir eine komponentenweise **Vektoraddition**
$\oplus: \mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}^n$ durch

$$(x_1, x_2, \ldots, x_n) \oplus (y_1, y_2, \ldots, y_n) = (x_1 + y_1, x_2 + y_2,
\ldots, x_n+y_n).$$

Weiterhin definieren wir eine komponentenweise Multiplikation mit einem Skalar
$\odot:\mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}^n$ durch

$$s\odot (x_1, x_2, \ldots, x_n) = (s\cdot x_1, s\cdot x_2, \ldots, s\cdot
x_n),$$

die **Skalarmultiplikation** genannt wird. Den Begriff **Skalar** haben wir hier
genommen, um zu verdeutlichen, dass $s$ nicht ein n-Tupel ist, sondern (in
diesem Fall) eine reelle Zahl. Mit den beiden Rechenoperationen »Vektoraddition«
und »Skalarmultiplikation« wird das reelle kartesische Produkt $\mathbb{R}^n$ zu
einem reellen **Vektorraum**, der auch **reeller Standardvektorraum** genannt
wird. Die n-Tupel mit Rechenoperationen werden daher auch **Vektoren** genannt.
Was genau ein Vektorraum ist, behandeln wir im nächsten Abschnitt. Zunächst
halten wir noch eine alternative Schreibweise fest.

Die Vektoren des reellen Standardvektorraumes werden häufig als sogenannte
**Spaltenvektoren** notiert. Das erleichtert die Übersicht bei der
Vektoraddition und der Skalarmultiplikation, da dann zeilenweise addiert und
mulitpliziert werden kann. Die Vektoraddition in Form von Spaltenvektoren wird
dann folgendermaßen notiert:

$$\begin{pmatrix}x_1 \\x_2\\ \vdots \\ x_n\end{pmatrix} + \begin{pmatrix}y_1
\\y_2\\ \vdots \\ y_n\end{pmatrix} = \begin{pmatrix}x_1 + y_1 \\x_2 + y_2\\
\vdots \\ x_n + y_n\end{pmatrix}.$$

Insbesondere wird meist das Symbol $\oplus$ vereinfacht als $+$ geschreiben, da
eine »normale« Addition nicht gemeint sein kann. Die Skalarmultiplikation wird
folgendermaßen geschrieben:

$$s\cdot \begin{pmatrix}x_1 \\x_2\\ \vdots \\ x_n\end{pmatrix} 
= \begin{pmatrix}s\cdot x_1 \\ s\cdot x_2 \\ \vdots \\ s\cdot x_n \end{pmatrix}.$$

Auch hier wird in der Regel anstatt des Symbols $\odot$ nur das normale
Multiplikationszeichen $\cdot$ verwendet, da jeweils aus dem Zusammenhang klar
ist, ob die normale Multiplikation zwischen reellen Zahlen oder die
Skalarmultiplikation gemeint ist. 


## Vektorraum 

Noch haben wir nicht die Frage beantwortet, was ein Vektorraum eigentlich ist.
Ein Vektorraum ist eine mathematische Struktur, die über einem Körper definiert
ist. Da wir hier nicht den Begriff Körper erläutern wollen, beschränken wir uns
auf das prominente Beispiel der reellen Zahlen als Körper. Details zu Körpern
können beispielsweise in dem [Wikipedia-Artikel → Körper
(Algebra)](https://de.wikipedia.org/wiki/Körper_(Algebra)) nachgelesen werden.

Zu dem Körper (also hier den reellen Zahlen) kommt noch eine weitere Menge, die
wir mit $V$ abkürzen. In unserem obigen Beispiel war als $V$ die Menge der
n-Tupel gewählt worden. Ein anderes Beispiel könnte aber auch die Menge $V$ die
Funktionen $\{1, x, x^2, \ldots, x^n\}$ sein.

Als dritte und vierte Zutat für einen Vektorraum kommen noch zwei Verknüpfungen
(Rechenoperationen) dazu:

* Vektoraddition $\oplus: V \times V \to V$ und
* Skalarmultiplikation $\odot: \mathbb{R} \times V \to V$.

Der Körper (hier $\mathbb{R}$), die Menge $V$ und die beiden Verknüpfungen
$\oplus$ und $\odot$ bilden einen Vektorraum, wenn für alle $u, v, w \in V$ und
$s,t \in \mathbb{R}$ die folgende Eigenschaften gelten:

Vektoraddition:
1. Assoziativgesetz: $u\oplus(v\oplus w) = (u\oplus v)\oplus w$
2. Existenz eines neutralen Elements $0\in V$ mit $v\oplus 0 = 0\oplus v = v$
3. Existenz eines zu $v\in V$ inversen Elements $-v\in V$ mit $v\oplus (-v)=
   (-v)\oplus v = 0$
4. Kommutativgesetz: $v\oplus u = u \oplus v$

Skalarmultiplikation:
1. Vektorielles Distributivgesetz: $s\odot(u\oplus v) = (s\odot u) \oplus
   (s\odot v)$
2. Skalares Distributivgesetz: $(s+t)\odot v = (s\odot v) \oplus (t\odot v)$
3. Assoziativgesetz für Skalare: $(s\cdot t)\odot v = s\odot (t \odot v)$
4. Existenz eines neutralen Elements: $1\odot v = v$

In der Physik wird der Raum unserer Anschauung oft als **euklidischer Raum**
bezeichnet. Es gibt verschiedene Interpretationen dieses Begriffes. Eine davon
ist, den euklidischen Raum als reellen Standardvektorraum zu interpretieren. In
den folgenden Videos wird daher nicht zwischen beiden Begriffen unterschieden.

```{dropdown} Video "n-dimensionaler euklidischer Raum" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/uh14yOb_0VY" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Addition von Vektoren" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/IN_21Zd8tcE" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Skalarmultiplikation" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/dz3ccb5cqxQ" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

```{dropdown} Video "Subtraktion von Vektoren" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/9oQzrH0x434" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```


## Zusammenfassung und Ausblick

Der mathematische Begriff Vektorraum ist zunächst recht abstrakt. In dieser
Vorlesung beschränken wir uns auf daher auf reelle Vektorräume. Im nächsten
Kapitel werden wir den reellen Standardvektorraum benutzen, um geometrische
Objekte zu beschreiben.












