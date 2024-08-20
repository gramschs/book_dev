# 3.5 Betrag Vektor und Abstand Punkte

Nachdem wir im letzten Kapitel den affinen Punkt kennengelernt haben, führen wir
nun noch den Betrag von Vektoren ein. Streng genommen, wird so aus dem
Vektorraum ein normierter Raum.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie wissen, was der **Betrag** eines Vektors ist und können ihn ausrechnen.
* Sie können den **Einheitsvektor** in Richtung eines Vektors bestimmen
  (=**normieren**).
* Sie können den **Abstand zweier Punkte** berechnen.
* Sie können den **Mittelpunkt zweier Punkte** berechnen.
```

## Betrag eines Vektors

Der Betrag eines Vektors ist geometrisch interpretiert die Länge des Pfeils,
also der Verschiebung. Wird das kartesische Koordinatensystem genutzt, können
wir eine Formel zu Berechnung des Betrages angeben. Ist $\vec{v}\in
\mathbb{R}^n$ ein Vektor, so wird sein Betrag mit dem Symbol

$$|\vec{v}| \; \text{ oder } \; ||\vec{v}||$$

abgekürzt. Um nun den Betrag eines Vektors des reellen Standardvektors berechnen
zu können, fertigen wir zunächst eine Skizze an. Als Beispiel nehmen wir einen
Vektor $v\in\mathbb{R}^2$ mit

$$\vec{v} = \begin{pmatrix} 6 \\ 2.5 \end{pmatrix}.$$

Es gibt unendlich viele Pfeile, die geometrisch diesen Vektor im kartesischen
Koordinatensystem repräsentieren. In der Skizze haben wir die Verschiebung
eingezeichnet, die beim Punkt $(1.5, 2)$ startet.

```{figure} pics/ betrag_vektor.png
---
width: 75%
name: betrag_vektor
---
Beispiel eines Vektors im $\mathbb{R}^2$; Quelle: eigene Darstellung; Lizenz: [CC BY-SA
4.0](https://creativecommons.org/licenses/by-sa/4.0)
```

Ergänzen wir jetzt zwei Strecken wie in der Skizze ersichtlich, so ergibt sich
ein rechtwinkliges Dreieck. Die Länge der Katheten entspricht den Elementen des
Vektors. Daher können wir mit dem Satz des Pythagoras direkt die Länge bzw. den
Betrag $|\vec{v}|$ des Vektors berechnen:

$$|\vec{v}| = \sqrt{6^2 + 2.5^2} = \sqrt{42.25} = 6.5.$$

Dieses Vorgehen können wir verallgemeinern. Allgemein kann der Betrag
$|\vec{v}|$ eines Vektors

$$\vec{v} = \begin{pmatrix} v_1 \\ v_2 \\ \vdots \\ v_2 \end{pmatrix}$$

des reellen Standardvektorraumes $\mathbb{R}^n$ folgendermaßen berechnet werden:

$$|\vec{v}| = \sqrt{v_1^2 + v_2^2 + \ldots + v_n^2}.$$

```{dropdown} Video "Betrag / euklidische Norm" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/zFKvZpzzO7M" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

## Einheitsvektor bzw. Vektoren normieren  

Ein Vektor, der die Länge bzw. den Betrag Eins hat, für den also $|\vec{v}|=1$
gilt, wird **Einheitsvektor** genannt. Beispielsweise ist der Vektor

$$\vec{v} = \begin{pmatrix} 0.1 \\ 0.5 \\ 0.7 \\ 0.5 \end{pmatrix}$$

ein Einheitsvektor, denn es gilt

$$|\vec{v}| = \sqrt{0.1^2 + 0.5^2 + 0.7^2 + 0.5^2} = \sqrt{1/100 + 25/100 +
49/100 + 25/100} = 1.$$

Sehr häufig ist ein Vektor kein Einheitsvektor. In den Ingenieurwissenschaften
wird jedoch oft gefordert, Richtungen durch Einheitsvektoren zu beschreiben. Es
gibt die Möglichkeit, aus jedem Vektor (wenn es nicht gerade der Nullvektor
ist), einen Einheitsvektor zu machen. Diesen Vorgang nennt man **Normierung**.
Ein Vektor wird normiert, indem jede Komponente durch den Betrag des Vektors
geteilt wird. In unserem obigen Beispiel galt

$$\vec{v} = \begin{pmatrix} 6 \\ 2.5 \end{pmatrix} \Rightarrow |\vec{v}| =
6.5.$$

Teilen wir die beiden Komponenten jeweils durch $6.5=\frac{13}{2}$, erhalten wir
den normierten Vektor

$$\vec{e}_v = \begin{pmatrix} \frac{12}{13} \\ \frac{5}{13} \end{pmatrix}.$$

Einheitsvektoren, die durch Normierung aus einem Vektor $\vec{v}$ entstanden
sind, werden üblicherweise als $\vec{e}_{v}$ notiert. Wir rechnen noch nach, ob
der Vektor $\vec{e}_v$ tatsächlich ein Einheitsvektor ist:

$$|\vec{e}_v| = \sqrt{\left(\frac{12}{13}\right)^2 + \left(\frac{5}{13}\right)^2}
= \sqrt{\frac{144}{169}+\frac{25}{169}} = \sqrt{\frac{169}{169}} = 1.$$

Allgemein lautet die Formel zur Normierung eines Vektors $\vec{v}$

$$\vec{e}_v = \frac{1}{|\vec{v}|} \vec{v}.$$

```{dropdown} Video "Vektor normieren (Normalenvektor Einheitsvektor)" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/03fcWnj6f4g?si=Lmb0X22BRUU3zjL9" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Abstand zweier Punkte

Bisher haben wir nur Vektoren betrachtet bzw. ihre geometrische Interpretation
als Verschiebung. Als nächstes greifen wir wieder auf das Konzept des affinen
Punktraumes $\mathbb{R}^n$ zurück und nutzen es, um den Abstand zweier Punkte im
$\mathbb{R}^n$ zu berechnen.  

Die beiden Punkte nennen wir $P$ und $Q$ und ihre Koordinaten werden
entsprechend als $P(P_1, P_2, \ldots, P_n)$ und $Q(Q_1, Q_2, \ldots, Q_n)$
bezeichnet. Weil der reelle Standardvektorraum $\mathbb{R}^n$ ein affiner
Punktraum ist, muss ein Vektor $\vec{v}$ existieren, der $P$ und $Q$ verbindet,
also

$$P + \vec{v} = Q.$$

Im vorherigen Kapitel haben wir schon gelernt, dass dieser Vektor aus den
komponentenweisen Differenzen der Punktkoordinaten besteht:

$$\vec{v} = \begin{pmatrix} Q_1 - P_1 \\ Q_2 - P_2 \\ \vdots \\ Q_n - P_n
\end{pmatrix}.$$

Von diesem Vektor brauchen wir also nur noch den Betrag berechnen, um den
Abstand $d(P,Q)$ zwischen dem Punkt $P$ und dem Punkt $Q$ zu erhalten:

$$d(P,Q) = \sqrt{(Q_1 - P_1)^2 + (Q_2 - P_2)^2 + \ldots + (Q_n - P_n)^2}.$$

Das »d« steht dabei für das Wort **Distanz**.

```{dropdown} Video zu "Abstand zweier Punkte" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/eXSMrAB-miM" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

## Mittelpunkt einer Strecke berechnen

Sind zwei Punkte $P$ und $Q$ gegeben, können wir die Richtung zwischen den
beiden Punkten als

$$\overrightarrow{PQ} = \begin{pmatrix} Q_1 - P_1 \\ Q_2 - P_2 \\ \vdots \\ Q_n - P_n
\end{pmatrix}$$

angeben. Ist nun die Position den Punktes $M$ als Mittelpunkt zwischen $P$ und
$Q$ gefragt, so müssen wir den Punkt $P$ um die Hälfte von $\overrightarrow{PQ}$
verschieben. Es gilt also

$$M = P + \frac{1}{2}\vec{PQ}.$$

```{dropdown} Video "Vektorrechnung Mittelpunkt berechnen" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/63yukPX43tI?si=YBWaylBuFar8LU1E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

In diesem Kapitel haben wir den Betrag/Länge eines Vektors kennengelernt. Zum
einen wird der Betrag benötigt, um bei technischen Problemen die Größe eines
Vektors zu bestimmen (z.B. Größe/Stärke der Kraft), zum anderen werden Vektoren
häufig normiert, um nur die Richtung anzugeben. Mit Hilfe des Betrages können
wir darüber hinaus den Abstand oder den Mittelpunkt zweier Punkte berechnen.
