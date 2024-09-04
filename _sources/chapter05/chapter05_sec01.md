# 5.1 Geraden

Bisher haben wir Geraden in einer Ebene betrachtet. In diesem Kapitel wollen wir
Geraden im dreidimensionalen euklidischen Raum $\mathbb{R}^3$ kennenlernen.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie können eine Geradengleichung aufstellen, wenn *ein Punkt und ein
  Richtungsvektor* gegeben sind. Diese Form der Geradengleichung nennt man
  **Parameterdarstellung einer Geraden**.
* Sie können eine Geradengleichung aufstellen, wenn *zwei Punkte* gegeben sind.
```

## Parameterdarstellung einer Geraden

Eine Gerade ist eine unendlich lange, unendlich dünne, gerade Linie. Sie kann
als eine Menge von unendlichen vielen Punkten beschrieben werden. Gehen wir
zunächst einmal davon aus, dass wir einen Punkt kennen, der Teil der Gerade ist.
Diesen Punkt nennen wir $P$. Kennen wir einen zweiten Punkt $Q$, der Teil der
Gerade ist, dann können wir den sogenannten **Richtungsvektor** $\vec{u}$
einführen, der die beiden Punkte $P$ und $Q$ verbindet:

$$\vec{u} = \overrightarrow{PQ}.$$

Dann können wir jeden Punkt $X$ der Gerade erreichen, indem wir bei $P$ starten
und ein Vielfaches des Richtungsvektors $\vec{u}$ addieren. Wir schreiben

$$X = P + s\cdot\vec{u}$$

mit dem **Parameter** $s\in\mathbb{R}$.

Für jeden Wert des Parameters $s$ erhalten wir einen anderen Punkt auf der
Geraden und umgekehrt. Um diese Abhängigkeit vom Parameter $s$ auszudrücken,
wird auch manchmal die folgende Notation verwendet:

$$X(s) = P + s\cdot\vec{u}.$$

```{admonition} Wie lautet ... die Parameterdarstellung der Geraden?
:class: note
Eine Gerade $g$ ist eine Menge aus Punkten, die sich schreiben lässt als

$$g = \{X \,|\, X = P + s\cdot\vec{u}, \; s\in\mathbb{R}\}.$$

Wir notieren auch kurz $g: X = P + s\cdot\vec{v}, \; s\in\mathbb{R}$.
```

Das folgende Video erklärt die Parameterdarstellung einer Gerade. Bei Zeitmarke
3:20 min können Sie das Video stoppen, da wir die Lage von Geraden erst in einem
späteren Kapitel behandeln werden.

```{dropdown} Video "Geraden im Raum" von Flip the Classroom
<iframe width="560" height="315" src="https://www.youtube.com/embed/qCRN2Qsm0D0?si=FsRvv59nTluEzxQX" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

Nachdem wir hier die Parameterdarstellung einer Gerade kennengelernt haben,
werden wir uns im nächsten Kapitel mit Ebenen beschäftigen. Auch bei
Ebenengleichungen gibt es eine Parameterdarstellung. Für viele geometrische
Anwendungen ist aber eine alternative Darstellung zweckmäßiger, die sogenannte
Normalengleichung, eine parameterfreie Gleichung zur Beschreibung einer Ebene.
