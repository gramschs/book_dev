# 4.3 Geometrische Interpretation Skalarprodukt

In diesem Kapitel werden wir das Skalarprodukt für Vektoren in der Geometrie
anwenden. Wir setzen ein kartesisches, dreidimensionales Koordinatensystem
voraus und stellen Verschiebungen bzw. Bewegungen bzgl. dieses
Koordinatensystems als Vektoren des Standardvektorraumes $\mathbb{R}^3$ dar.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie kennen den Zusammenhang zwischen Skalarprodukt und Betrag/Länge eines
  Vektors: 

  $$|\vec{a}|=\sqrt{\vec{a}\cdot\vec{a}}.$$

* Sie wissen, welche Bedeutung das **Skalarprodukt** zweier Vektoren **geometrisch**
  hat: Das Skalarprodukt der Vektoren $\vec{a}$ und $\vec{b}$
  ist das Produkt aus den Längen der beiden Vektoren und dem Kosinus des von den
  beiden Vektoren eingeschlossenen Winkels $\varphi = \angle (\vec{a},\vec{b})$:

  $$\vec{a}\cdot\vec{b} = |\vec{a}|\cdot|\vec{b}| \cdot \cos(\varphi).$$

* Sie können den **Winkel zwischen zwei Vektoren** berechnen, wenn Sie das
  Skalarprodukt und die beiden Längen kennen:

  $$\varphi = \arccos\left(\frac{\vec{a}\cdot\vec{b}}{|\vec{a}|\cdot|\vec{b}|}\right),
  \quad \vec{a}\neq\vec{0}, \vec{b}\neq\vec{0}.$$

```

## Skalarprodukt und Betrag/Länge von Vektoren

Für Vektoren des reellen Standardvektorraumes $\vec{x}\in\mathbb{R}^n$ ist der
Betrag des Vektors definiert als

$$|\vec{x}| = \sqrt{x_1^2 + x_2^2 + \ldots + x_n^2}.$$

Im geometrischen Kontext wird oft der Begriff »Länge eines Vektors« anstatt
»Betrag eines Vektors« verwendet. Das liegt an der Interpretation des
geometrischen Vektors als Verschiebung. Ist ein Vektor $\vec{v}\in\mathbb{R}^3$
gegeben und ist $P$ ein beliebiger Punkt in einem kartesischen
3D-Koordinatensystem, dann führt die Verschiebung $\vec{v}$ zu einem neuen
Punkt $Q$, also $P = \vec{v} = Q$. Die Länge der Strecke zwischen den Punkten
$P$ und $Q$ ist gleich dem Betrag des Vektors $\vec{v}$, also

$$\overline{PQ} = \sqrt{v_1^2 + v_2^2 + v_3^2} = |\vec{v}|.$$

Wenn wir jetzt das Skalarprodukt von $\vec{v}$ mit sich selbst berechnen, erhalten wir

$$\vec{v}\cdot\vec{v} =
\begin{pmatrix} v_1 \\ v_2 \\ v_3 \end{pmatrix} \cdot
\begin{pmatrix} v_1 \\ v_2 \\ v_3 \end{pmatrix} =
v_1^2 + v_2^2 + v_3^2.$$

Das ist genau der Ausdruck, der beim Betrag bzw. der Länge des Vektors unter der
Wurzel steht. Wir können also auch das Skalarprodukt eines Vektors mit sich
selbst nutzen, um den Betrag bzw. die Länge des Vektors zu berechnen:

$$|\vec{v}|=\sqrt{\vec{v}\cdot\vec{v}}.$$

Alternativ können wir auch die Formel

$$|\vec{v}|^2 = \vec{v}\cdot\vec{v}$$

nutzen.

```{dropdown} Video "Zusammenhang Skalarprodukt und Länge Vektor" von Mathehoch13
<iframe width="560" height="315" src="https://www.youtube.com/embed/Zjc7aI8cp4o?si=EMLwSAnLYt8aC01V" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; 
clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Skalarprodukt und eingeschlossener Winkel

Als nächstes führen wir den eingeschlossenen Winkel zwischen zwei Vektoren ein.
Geometrisch interpretieren wir die beiden Vektoren $\vec{a}\in\mathbb{R}^3$ und
$\vec{b}\in\mathbb{R}^3$ als Verschiebungen, die beide an einem gemeinsamen
Punkt starten. Unabhängig von der Reihenfolge der Vektoren wird der *kleinere*
Winkel zwischen den beiden Vektoren $\vec{a}$ und $\vec{b}$ als
**eingeschlossener Winkel** bezeichnet. Er  liegt somit zwischen 0 und 180°
(Gradmaß) bzw. zwischen 0 und $\pi$ (Bogenmaß). Wir verwenden für den
eingeschlossenen Winkel das Symbol $\angle (\vec{a},\vec{b})$ oder den
griechischen Buchstaben Phi $\varphi$.

```{figure} pics/eingeschlossener_winkel.png
---
width: 50%
name: eingeschlossener_winkel
---
Eingeschlossener Winkel $\varphi = \angle (\vec{a},\vec{b})$ zwischen den Vektoren $\vec{a}$ 
und $\vec{b}$; 
Quelle: eigene Darstellung, 
Lizenz: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0)
```

Wenn die beiden Vektoren $\vec{a}$ und $\vec{b}$ die gleiche Richtung haben und
gleich orientiert sind, ist $\varphi = 0^{\circ}$ (bzw. $\varphi=0$ im Bogenmaß).
Falls sie die gleiche Richtung haben, aber entgegengesetzt orientiert sind, gilt
für den eingeschlossenen Winkel $\varphi = 180^{\circ}$ (bzw. $\varphi = \pi$ im
Bogenmaß).

Als nächstes führen wir noch einen Vektor $\vec{c}$ als Differenz der beiden
Vektoren $\vec{a}$ und $\vec{b}$ ein, also

$$\vec{c} = \vec{b} - \vec{a}.$$

Da $\vec{a} + \vec{b} + \vec{c} = \vec{a} + \vec{b} + (\vec{b}-\vec{a}) =
\vec{0}$ der Nullvektor ist, liegt ein Polygonzug bzw. eine Vektorkette vor. Die
drei Vektoren sind die gerichteten Seiten eines Dreiecks, wie die folgende
Abbildung zeigt.

```{figure} pics/kosinussatz.png
---
width: 50%
name: kosinussatz
---
Kosinussatz; Quelle: eigene Darstellung, 
Lizenz: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0)
```

Für das Dreieck gilt der **Kosinussatz**:

```{math}
:label: chap08sec03eq01
|\vec{c}|^2 = |\vec{a}|^2 + |\vec{b}|^2 - 2\cdot |\vec{a}| \cdot
|\vec{b}|\cdot\cos(\varphi).
```

Da aber $\vec{c} = \vec{a} - \vec{b}$ gilt, können wir mit Hilfe der 2.
binomischen Formel den Term $|\vec{c}|^2$ durch das Skalarprodukt von
$(\vec{a}-\vec{b})$ mit sich selbst ersetzen:

\begin{align*}
|\vec{c}|^2 &= |\vec{a}-\vec{b}|^2 = \\
&= (\vec{a}-\vec{b}) \cdot (\vec{a}-\vec{b}) = \\
&= \vec{a}\cdot\vec{a} - 2\cdot\vec{a}\cdot\vec{b} + \vec{b}\cdot\vec{b}.
\end{align*}

Letzteres setzen wir nun auf der linken Seite von Gleichung
{eq}`chap08sec03eq01` ein:

$$\vec{a}\cdot\vec{a} - 2\cdot\vec{a}\cdot\vec{b} + \vec{b}\cdot\vec{b} =
|\vec{a}|^2 + |\vec{b}|^2 - 2\cdot |\vec{a}| \cdot |\vec{b}|\cdot\cos(\varphi).$$

Jetzt können wir ausnutzen, dass $\vec{a}\cdot\vec{a} = |\vec{a}|^2$ gilt und
$\vec{b}\cdot\vec{b} = |\vec{b}|^2$ und die Terme auf beiden Seiten der
Gleichung subtrahieren. Es bleibt die Gleichung

$$- 2\cdot\vec{a}\cdot\vec{b} =
- 2\cdot |\vec{a}| \cdot |\vec{b}|\cdot\cos(\varphi)$$

übrig. Zuletzt teilen wir noch auf beiden Seiten durch $(-2)$ und erhalten

$$\vec{a}\cdot\vec{b} = |\vec{a}|\cdot|\vec{b}| \cdot \cos(\varphi).$$

Das ist die geometrische Interpretation des Skalarproduktes im $\mathbb{R}^3$.

```{admonition} Was ist die geometrische Interpretation des Skalarproduktes?
:class: note
Im $\mathbb{R}^3$ kann das Skalarprodukt der beiden Vektoren
$\vec{a}\in\mathbb{R}^3$ und $\vec{b}\in\mathbb{R}^3$ über die Längen der
Vektoren und den eingeschlossenen Winkel $\varphi = \angle (\vec{a}, \vec{b})$
gemäß der Formel

$$\vec{a}\cdot\vec{b} = |\vec{a}|\cdot|\vec{b}| \cdot \cos(\varphi)$$

berechnet werden.
```

```{dropdown} Video "Herleitung Skalarprodukt"von Mathehoch13
<iframe width="560" height="315" src="https://www.youtube.com/embed/RQ_7laap-rM?si=AZQR6LYFfESZBuoy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Winkelberechnungen mit dem Skalarprodukt

Das Skalarprodukt der Vektoren $\vec{a}$ und $\vec{b}$ kann über die
Beträge/Längen der Vektoren $|\vec{a}|$ und $|\vec{b}|$ sowie dem Kosinus-Wert
des eingeschlossenen Winkels $\varphi = \angle (\vec{a},\vec{b})$ berechnet
werden. Sofern die beiden Vektoren $\vec{a}$ und $\vec{b}$ nicht der Nullvektor
sind, also $\vec{a}\neq\vec{0}$ bzw. $\vec{b}\neq\vec{0}$ gelten, können wir die
obige Formel auch umkehren. Aus dem Skalarprodukt kann dann mit Hilfe der
Arkuskosinus-Funktion der Winkel $\varphi$ berechnet werden:

$$\varphi =
\arccos\left(\frac{\vec{a}\cdot\vec{b}}{|\vec{a}|\cdot|\vec{b}|}\right),
\quad \vec{a}\neq\vec{0}, \vec{b}\neq\vec{0}.
$$

```{admonition} Mini-Übung
:class: miniexercise
Gehen Sie auf die Seite
https://o-mathe.de/analytische-geometrie/skalarprodukt/skalarprodukt/untersuchungen/lernstrecke
und machen Sie Aufgabe 1.
```

Aus dieser Beziehung können einige Schlussfolgerungen gezogen werden:

- Sind $\vec{a}$ und $\vec{b}$ parallel und gleichorientiert, ist also der
  eingeschlossene Winkel $\varphi = 0$, dann gilt

   $$\vec{a}\cdot\vec{b} = |\vec{a}| \cdot |\vec{b}|.$$

- Sind $\vec{a}$ und $\vec{b}$ parallel und entgegengesetzt orientiert, gilt
  also für den eingeschlossenen Winkel $\varphi = \pi$, dann gilt

  $$\vec{a}\cdot\vec{b} = - |\vec{a}| \cdot |\vec{b}|.$$

- Sind die beiden Vektoren $\vec{a}$ und $\vec{b}$ orthogonal (stehen senkrecht
  aufeinander), dann gilt

  $$\vec{a}\cdot\vec{b} = 0.$$

- Ist $\varphi$ ein spitzer Winkel, so gilt

  $$\vec{a}\cdot\vec{b} > 0.$$

- Ist $\varphi$ ein stumpfer Winkel, so gilt

  $$\vec{a}\cdot\vec{b} < 0.$$

Die große Bedeutung des Skalarproduktes in der Geometrie erkennen Sie daran,
dass es sehr viele Erklärvideos zu diesem Thema gibt. Einige Videos zu dem Thema
sind im Folgenden gelistet.

```{dropdown} Video "geometrische Interpretation Skalarprodukt" von Visual X
<iframe width="560" height="315" src="https://www.youtube.com/embed/swMhAjkoCm0?si=XPKYIezPvpQ7HqKf" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Mit Skalarprodukt Winkel berechnen" von Mathehoch13
<iframe width="560" height="315" src="https://www.youtube.com/embed/B96OVZR0F6A?si=18KQzQG_bBQww8Dc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;
 encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Winkel zwischen zwei Vektoren" von Mathematrick
<iframe width="560" height="315" src="https://www.youtube.com/embed/vB9yjxpbDQ4?si=QIH86HSQJf915iRr" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Standard Skalarprodukt Einfach Erklärt" von MathePeter
<iframe width="560" height="315" src="https://www.youtube.com/embed/wJAniAr6avU?si=E2-wbANRbD2VElRh" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Skalarprodukt Teil 2 |  Erklärung & Bedeutung" von Einfach Mathe!
<iframe width="560" height="315" src="https://www.youtube.com/embed/rZ1zS3MBV0Y?si=0SEe5f51bsH965WF" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

```{dropdown} Video "Skalarprodukt II" von Mathematische Methoden
<iframe width="560" height="315" src="https://www.youtube.com/embed/uGs7vGAxJko?si=YYM3r12agb-6C_tf" 
title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; 
encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

## Zusammenfassung und Ausblick

In diesem Kapitel haben wir die geometrische Interpretation des Skalarproduktes
kennengelernt. Einige Autoren von Mathematikbüchern gehen den umgekehrten Weg
und definieren das Skalarprodukt über die Formel $\vec{a}\cdot\vec{b} =
|\vec{a}|\cdot|\vec{b}| \cdot \cos(\varphi)$. Im nächsten Kapitel werden wir die
Anwendungen des Skalarproduktes in der Geometrie (und damit in Physik und
Technische Mechanik) weiter vertiefen.
