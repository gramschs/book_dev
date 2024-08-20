# 4.1 Basis und Dimension

In diesem Kapitel werden wir uns mit den grundlegenden Konzepten Basis und
Dimension von Vektorräumen beschäftigen. Beide Konzepte basieren auf der
Linearkombination von Vektoren, die wir im letzten Kapitel kennengelernt haben.

## Lernziele

```{admonition} Lernziele
* Sie wissen, was ein **Erzeugendensystem** ist.
* Sie wissen, was eine **Basis** ist.
* Sie wissen, was die **Dimension** eines Vektorraumes ist.
```

## Erzeugendensystem

Bei manchen vor allem hochpreisigen Gaming-Tastaturen wird damit geworben, dass
die Tastaturkappen für die Buchstaben W, A, S und D austauschbar sind. Doch
warum? Bei vielen Computerspielen werden diese vier Tasten zur Steuerung der
Spielfigur benutzt. Beispielsweise steuert A eine Figur nach links und D nach
rechts, während mit W die Figur nach oben und mit S nach unten gesteuert wird.
Bei einem zweidimensionalen Spiel reichen die Bewegungen oben/unten und
links/rechts aus, um jede Position des Spielfeldes zu erreichen. Somit kann die
Spielfigur komplett mit der linken Hand gesteuert werden und die rechte Hand
bleibt frei, um weitere Aktionen der Spielfigur zu kontrollieren.

Die Bewegung oben/unten wird von dem Computerspiel folgendermaßen interpretiert.
Jeder Tastendruck von W bewirkt, dass die Spielfigur einen Schritt nach oben
bewegt wird. Wird dreimal gedrückt, ist die neue y-Koordinate der Spielfigur

$$y_{\text{neu}} = y_{\text{alt}} + 3$$

und die reine Bewegung in y-Richtung $v_y = 3$. Wird danach fünfmal die S-Taste
gedrückt, bewegt sich die Spielfigur um fünf Schritte nach unten. Nimmt man
jetzt beide Bewegungen zusammen, dann ist die neue y-Position

$$y_{\text{neu}} = \left( y_{\text{alt}} + 3 \right) - 5 = y_{\text{alt}} -2.$$

Allgemein können wir die Bewegung der Spielfigur beschreiben als
Linearkombination

$$v_y = W \cdot (+1) + S \cdot (-1),$$

wobei die $+1$ für einen Schritt nach oben steht und die $-1$ für einen Schritt
nach unten.

Analog dazu können wir die Bewegung links/rechts durch die Tasten A und D
beschreiben. Wird erst dreimal die Taste A gedrückt und dann einmal die Taste D,
so läuft die Spielfigure drei Schritte nach links und dann einen Schritt nach
rechts. Insgesamt befindet sich die Figure dann zwei Schritte links von der
ursprünglichen Position, also

$$x_{\text{neu}} = x_{\text{alt}} - 2.$$

Die reine Bewegung können wir durch

$$v_x = D\cdot (+1) + A \cdot (-1)$$

berechnen. Diesmal steht $+1$ für einen Schritt nach rechts und $-1$ für einen
Schritt nach links.

Jetzt beschreiben wir die beiden Bewegungsarten gemeinsam. Fünfmal W, dreimal D
und dann zweimal A bedeutet, dass die Spielfigur am Ende der Bewegung fünf
Schritte nach oben und einen Schritt nach rechts gegangen ist. Wir nutzen die
Vektornotation, d.h. Bewegungen links/rechts werden als erste Komponente notiert
und die zweite Komponente repräsentiert die Bewegung oben/unten. Die drei
Bewegungen sind also

$$\vec{v} = \begin{pmatrix} 0 \\ 5 \end{pmatrix} + \begin{pmatrix} 3 \\ 0
\end{pmatrix} + \begin{pmatrix} -2 \\ 0 \end{pmatrix}.$$

Allgemein können wir jede Bewegung der Spielfigur folgendermaßen zusammensetzen:

$$\vec{v} = W \cdot \begin{pmatrix} 0 \\ 1 \end{pmatrix}
+ A \cdot \begin{pmatrix} -1 \\ 0 \end{pmatrix}
+ S \cdot \begin{pmatrix} 0 \\ -1 \end{pmatrix}
+ D\cdot \begin{pmatrix} 1 \\ 0 \end{pmatrix}.$$

Diese *vier* Bewegungsvektoren erzeugen alle Bewegungen, um jede Position des
Spielfeldes zu erreichen. In der Mathematik nennt man eine Menge von Vektoren,
die linear kombiniert jeden Vektor des Vektorraumes erzeugen, ein
**Erzeugendensystem**.

Mathematisch präzise wird ein Erzeugendensystem folgendermaßen definiert.

```{admonition} Was ist ... ein Erzeugendensystem?
:class: note
Ist $V$ ein reeller Vektorraum, dann wird eine Menge $E\subseteq V$ von Vektoren
**Erzeugendensystem** von $V$ genannt, wenn jeder Vektor $\vec{v}\in V$ als
Linearkombination von den Vektoren aus $E$ dargestellt werden kann. Jeder Vektor
$\vec{v}\in V$ hat also eine Zerlegung der Form

$$\vec{v} = s_1\cdot \vec{e}_1 + s_2 \cdot \vec{e}_2 + \ldots + s_n \cdot
\vec{e}_n$$

mit den Skalaren $s_1, s_2, \ldots, s_n$ und den Erzeugendensystem-Vektoren
$\vec{e}_1, \vec{e}_2, \ldots, \vec{e}_n \in E$.
```

```{dropdown} Video "Erzeugendensystem" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/Yh8xj_iMe98?si=I7eRSZneTrPf9pvx" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Basis

Bei dem obigen Beispiel des Erzeugendensystems für ein 2D-Computerspiel haben
wir vier Vektoren benutzt, um die Bewegungen der Spielfigur auf dem Spielfeld zu
beschreiben:

$$\vec{v} = W \cdot \begin{pmatrix} 0 \\ 1 \end{pmatrix}
+ A \cdot \begin{pmatrix} -1 \\ 0 \end{pmatrix}
+ S \cdot \begin{pmatrix} 0 \\ -1 \end{pmatrix}
+ D\cdot \begin{pmatrix} 1 \\ 0 \end{pmatrix}.$$

Wenn wir als Spieler beobachten wollen, wie die Figur läuft, ist es sinnvoll
jede Einzelbewegung auch als solche zu animieren. Sollte das Computerspiel auch
einen Transport zulassen, bei der die Figur sich von einer Position zu einer
anderen Position teleportiert, ohne dass die Bewegung selbst sichtbar wird (z.B.
beim Spawnen), dann ist es einfacher, nur die Gesamtbewegung
$\vec{v}_{\text{gesamt}}$ zu betrachten:

$$\vec{v}_{\text{gesamt}} = \begin{pmatrix} 0 \\ 5 \end{pmatrix} + \begin{pmatrix} 3 \\ 0
\end{pmatrix} + \begin{pmatrix} -2 \\ 0 \end{pmatrix} =
\begin{pmatrix} 1 \\ 5 \end{pmatrix}.$$

Die Spielfigur teleportiert also zu der neuen Position

\begin{align*}
x_{\text{neu}} &= x_{\text{alt}} + 1, \\
y_{\text{neu}} &= y_{\text{alt}} + 5. \\
\end{align*}

Am einfachsten lässt sich die Teleportation durch ein Erzeugendensystem
beschreiben, bei dem nur zwei Vektoren verwendet werden. Der erste Vektor
beschreibt die Bewegung links/rechts, der zweite Vektor die Bewegung oben/unten:

$$\vec{v}_{\text{gesamt}} = (D - A) \cdot \begin{pmatrix} 1 \\ 0 \end{pmatrix} +
(W - s) \cdot \begin{pmatrix} 0 \\ 1 \end{pmatrix}.$$

Bei der Gesamtbewegung werden erst die resultierenden Schritte links/rechts als
$D-A$ berechnet und dann die resultierenden Schritte oben/unten als $W-S$.
Dennoch können wir immer noch jede Bewegung auf dem Spielfeld darstellen, die
gebraucht wird, um jede Position auf dem Spielfeld zu erreichen. Lassen wir
jedoch einen der beiden Vektoren weg und benutzen beispielsweise nur noch

$$\vec{v}_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix},$$

so können wir nur noch links/rechts-Bewegungen erzeugen. Die Spielfigure könnte
sich nur noch entlang einer horizontalen Linie bewegen, die auf der Höhe ihrer
Startposition liegt. Weniger als zwei Vektoren darf das Erzeugendensystem nicht
haben. Das minimale Erzeugendensystem, mit dem durch Linearkombination alle
Vektoren eines Vektorraums dargestellt werden können, nennt man **Basis**. Für
unser 2D-Computerspiel bildet die Menge

$$E = \left\{
\begin{pmatrix} 0 \\ 1 \end{pmatrix},
\begin{pmatrix} -1 \\ 0 \end{pmatrix},
\begin{pmatrix} 0 \\ -1 \end{pmatrix},
\begin{pmatrix} 1 \\ 0 \end{pmatrix}
\right\} $$

ein Erzeugendensystem. Die Menge

$$B = \left\{
\begin{pmatrix} 1 \\ 0 \end{pmatrix},
\begin{pmatrix} 0 \\ 0 \end{pmatrix}
\right\} $$

bildet eine Basis der Bewegungen auf dem Spielfeld.

```{admonition} Was ist ... eine Basis?
:class: note
Ein minimales Erzeugendensystem eines Vektorraumes wird **Basis** genannt. Damit
ist gemeint, dass alle Vektoren des Vektorraumes $V$ durch eine
Linearkombination der Vektoren von $B$ dargestellt werden können (=
Erzeugendensystem). Wird jedoch ein Element aus der Menge $B$ der Basisvektoren
entfernt, können nicht mehr alle Vektoren von $V$ durch Linearkombination
erzeugt werden (= minimal).
```

## Dimension

Offensichtlich ist die Anzahl der Basisvektoren eine wichtige Eigenschaft eines
Vektorraumes. Bei unserem Computerspiel führt die Eigenschaft, dass mindestens
zwei Basisvektoren gebraucht werden, um die Bewegungen links/rechts und
oben/unten zu beschreiben, dazu, dass vier Finger für die Steuerung der
Spielfigur benötigt werden. A - D steuern entlang des Vektors

$$\vec{b}_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$$

und W - S entlang

$$\vec{b}_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix}.$$

Wir könnten auch eine andere Basis wählen. Auch die Vektoren

$$B' = \left\{\begin{pmatrix} 1 \\ 1 \end{pmatrix}, \begin{pmatrix} -1 \\ 1 \end{pmatrix}
\right\}$$

ermöglichen es, jede Bewegung auf dem Spielfeld darzustellen. Die Spielfigure
bewegt sich dann diagonal auf dem Spielfeld, kann aber dennoch durch geschickte
Linearkombination jede Position des Spielfeldes erreichen. Aber auch hier
brauchen wir mindestens zwei Basisvektoren, damit die Spielfigure nicht auf eine
einzige Diagonale beschränkt ist.  

Da die Anzahl der Basisvektoren so wichtig zur Charakterisierung von
Vektorräumen ist, hat sie einen eigenen Namen. Die Anzahl der Basisvektoren wird
**Dimension** genannt. Sie ändert sich auch nicht, wenn die Basis gewechselt
wird.

```{admonition} Was ist ... die Dimension eines Vektorraumes?
Die Anzahl der Basisvektoren eines Vektorraumes $V$ wird **Dimension** genannt. Oft
wird sie mit dem mathematischen Symbol $\dim(V)$ abgekürzt.
```

Die Bewegungen unseres zweidimensionales Computerspiels werden also durch einen
Vektorraum der Dimension 2 beschrieben :-)

```{dropdown} Video "Basis und Dimension" von Prof. Hoever
<iframe width="560" height="315" src="https://www.youtube.com/embed/xhG2nXniUfA?si=meqKP2ryeKV9glv-" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

Die Basis ist ein wichtiges Konzept, um möglichst effizient alle Vektoren eines
Vektorraumes durch Linearkombination zur erzeugen. Die minimal notwendige Anzahl
an Vektoren, die dafür gebraucht wird, ist eine wichtige Eigenschaft und wird
als Dimension bezeichnet.
