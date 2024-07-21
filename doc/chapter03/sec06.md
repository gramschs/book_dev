# 3.6 Linearkombination und lineare Unabhängigkeit

In der Technischen Mechanik werden Kräfte oft zerlegt. Die Grundlage dafür
bilden Linearkombinationen und eindeutige Darstellungen der Zerlegungen, die nur
bei den sogenannten linear unabhängigen Vektoren möglich sind. Daher werden wir
uns in diesem Kapitel damit näher beschäftigen.

## Lernziele

```{admonition} Lernziele 
:class: goals
* Sie wissen, was eine **Linearkombination** von Vektoren ist.
* Sie wissen, was **linear abhängige** und **linear unabhängige** Vektoren sind.
* Sie können auch testen, ob gegebene Vektoren linear unabhängig sind.
```


## Linearkombination

Werden mehrere Vektoren mit einem Skalar multipliziert und dann summiert, so
nennt man das Ergebnis eine Linearkombination. Im einfachsten Fall werden zwei
Vektoren linear kombiniert, wie in dem folgenden Beispiel die beiden Vektoren
$\vec{v}$ und $\vec{w}$:

$$3\cdot\vec{v} + (-1.5)\cdot \vec{w}.$$

Das Ergebnis ist wieder ein Vektor. Wenn wir mehrere Vektoren haben, z.B. $m$
Stück, die wir $\vec{v}_1\in\mathbb{R}^n$, $\vec{v}_2\in\mathbb{R}^n$ bis
$\vec{v}_m\in\mathbb{R}^n$ nennen, und entsprechend viele Skalare $s_1, s_2,
\ldots, s_m$, dann ist die Linearkombination

$$\vec{w} = s_1\vec{v}_1 + s_2\vec{v}_2 + \ldots + s_m\vec{v}_m.$$

Interpretieren wir die Linearkombination geometrisch, bedeutet das, dass wir die
Verschiebung $\vec{v}_1$ mit $s_1$ strecken oder stauchen, dann die Verschiebung
$\vec{v}_2$ mit $s_2$ strecken oder stauchen und an das Ende von $s_1\vec{v}_1$
dranhängen und immer so weiter.

```{dropdown} Video "Linearkombination Definition" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/MawOKGC5Row" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

```{dropdown} Video "Linearkombination Beispiel" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/vYGBcIHfaso" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

```{dropdown} Video "Linearkombinationen" von VisualX
<iframe width="560" height="315" src="https://www.youtube.com/embed/wLel2yICtgA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

## Linearkombination berechnen

Wenn die Vektoren und die Skalare der Linearkombination gegeben sind, ist es
einfach, den entsprechenden resultierenden Vektor zu berechnen. Interessant für
technische Anwendungen ist jedoch vor allem die umgekehrte Fragestellung. Wenn
die Vektoren $\vec{v}_1$, $\vec{v}_2$ bis $\vec{v}_m$ gegeben sind, wie müssen
sie skaliert werden, so dass der Vektor $\vec{w}$ herauskommt? Welchen Wert
haben die Skalare $s_1$ bis $s_m$?

Bleiben wir bei einer Linearkombination mit zwei Vektoren:

$$s_1\cdot \begin{pmatrix} 2 \\ -1 \end{pmatrix} + 
s_2 \cdot \begin{pmatrix} 3 \\ 1 \end{pmatrix} = 
\begin{pmatrix} 19 \\ 3 \end{pmatrix}.$$

Wir können die Gleichung komponentenweise in Form eines linearen
Gleichungssystems hinschreiben:

\begin{align*}
2\cdot s_1 + 3\cdot s_2 &= 19 \\
-1\cdot s_1 + 1\cdot s_2 &= 3 
\end{align*}

Lösen des Gleichungssystems liefert $s_1 = 2$ und $s_2 = 5$, also

$$2\cdot \begin{pmatrix} 2 \\ -1 \end{pmatrix} + 
5 \cdot \begin{pmatrix} 3 \\ 1 \end{pmatrix} = 
\begin{pmatrix} 19 \\ 3 \end{pmatrix}.$$


## Lineare Unabhängigkeit

Wenn wir in dem obigen Beispiel einen dritten Vektor in die Linearkombination
einfügen, so können wir den Skalar davor Null setzen, denn die ersten beiden
Vektoren erfüllen ja schon die Gleichung:

$$2\cdot \begin{pmatrix} 2 \\ -1 \end{pmatrix} + 
5 \cdot \begin{pmatrix} 3 \\ 1 \end{pmatrix} +
0\cdot \begin{pmatrix} -1 \\ 3 \end{pmatrix}= 
\begin{pmatrix} 19 \\ 3 \end{pmatrix}.$$

Wir könnten jetzt die Skalare aber auch komplett anders wählen, die folgende
Linearkombination ergibt den gleichen resultierenden Vektor:

$$0\cdot \begin{pmatrix} 2 \\ -1 \end{pmatrix} + 
6 \cdot \begin{pmatrix} 3 \\ 1 \end{pmatrix} + (-1) \cdot \begin{pmatrix} -1 \\ 3 \end{pmatrix}= 
\begin{pmatrix} 19 \\ 3 \end{pmatrix}.$$

Es ist nicht verwunderlich, dass nach Einfügen des 3. Vektors die Skalare
beliebig gewählt werden können, da bereits der 3. Vektor eine Linearkombination
der ersten beiden ist:

$$(-2)\cdot \begin{pmatrix} 2 \\ -1 \end{pmatrix} + 
1 \cdot \begin{pmatrix} 3 \\ 1 \end{pmatrix} = 
\begin{pmatrix} -1 \\ 3 \end{pmatrix}.$$

Wenn ein Vektor $\vec{1}$ als Linearkombination von anderen Vektoren
$\vec{v}_2$, $\vec{v}_3$ bis $\vec{v}_m$ dargestellt werden kann, dann nennt man
diese Vektoren **linear abhängig**. Das Gegenteil davon heißt **linear
unabhängig**. Die genaue mathematische Definition ist wie folgt:

Ist $V$ ein reeller Vektorraum, dann heißen die Vektoren $\vec{v}_1, \vec{v}_2,
\ldots, \vec{v}_m$ aus $V$ linear unabhängig, wenn die einzig mögliche
Linearkombination des Nullvektors 

$$s_1\cdot\vec{v}_1 + s_2 \cdot \vec{v}_2 + \ldots + s_n \vec{v}_m = \vec{0}$$

bedeutet, dass alle Skalare Null sind, also $s_1 = s_2 = \dots = s_m = 0$ folgt.

```{dropdown} Video "Lineare Abhängigkeit" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/pLkde--khqs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

```{dropdown} Video "Lineare Unabhängigkeit - Definition" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/lrW95QKNfWA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

```{dropdown} Video "Lineare Unabhängigkeit - Beispiel 1" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/O85kVJrvc-g" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

```{dropdown} Video "Lineare Unabhängigkeit - Beispiel 2" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/nUs3G__ZX2c" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

```{dropdown} Video "Lineare Unabhängigkeit - Beispiel 3" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/Sd9RYIHtTLg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
</iframe>
```

## Zusammenfassung und Ausblick

Linearkombinationen und lineare Unabhängigkeit werden uns zu dem nächsten
mathematischen Konzept führen, der Basis von Vektorräumen.
