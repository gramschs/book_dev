# 4.4 Anwendungen Skalarprodukt

In Physik und Technischer Mechanik wird das Skalarprodukt häufig in seiner
geometrischen Interpretation genutzt, da es zahlreiche Anwendungen hat. Im
Folgenden beschäftigen wir uns mit den wichtigsten Anwendungen davon.

## Lernziele

```{admonition} Lernziele
:class: goals
* Sie können überprüfen, ob zwei Vektoren **kollinear** sind.
* Sie kennen das **Orthogonalitätskriterium** und können mit dem Skalarprodukt
  überpüfen, ob zwei Vektoren orthogonal $\perp$ (= senkrecht zueinander) sind.
* Sie können die **senkrechte Projektion** eines Vektors auf einen anderen
  Vektor berechnen.
* Sie können die **Richtungswinkel** eines Vektors mit den Koordinatenachsen
  berechnen.
```

## Kollinearität

Eine wichtige Anwendung des Skalarproduktes in der Geometrie ist zu überprüfen,
ob zwei Vektoren orthogonal sind. Bevor uns der Orthogonalität widmen,
betrachten wir zunächst parallele und antiparallele Vektoren. Geometrisch
interpretiert sind zwei Vektoren zueinander **parallel**, wenn sie die gleiche
Richtung haben. Liegen beide Vektoren auf derselben Geraden, aber haben sie
entgegengesetzte Richtungen, so sagt man, die beiden Vektoren sind
**antiparallel**. Beides fasst man als **kollinear** zusammen. Kollineare
Vektoren sind also entweder parallel oder antiparallel. Oder anders formuliert,
kollineare Vektoren liegen immer auf einer Geraden, nur die Richtung ist ggf.
entgegengesetzt.

```{admonition} Wann sind ... zwei Vektoren kollinear?
:class: note
Zwei Vektoren sind kollinear, wenn ein Vektor ein Vielfaches vom anderen Vektor
ist:

$$\vec{a} = s\cdot\vec{b}, \quad s\neq 0.$$

Ist der Skalar $s < 0$, so sind die beiden Vektoren $\vec{a}$ und $\vec{b}$
antiparallel. Ist hingegen $s > 0$, sind die beiden Vektoren parallel.
```

Zusammen mit dem Skalarprodukt ergeben sich dann die folgende
Schlussfolgerungen. Sind zwei Vektoren $\vec{a}$ und $\vec{b}$, die beide nicht
der Nullvektor sind, parallel, dann gilt

$$\vec{a}\cdot\vec{b} = |\vec{a}|\cdot|\vec{b}|.$$

Das ergibt sich aus der geometrischen Interpretation des Skalarproduktes, denn
der eingeschlossene Winkel ist bei parallelen Vektoren $\varphi =
\angle(\vec{a}, \vec{b}) = 0^{\circ}$ und $\cos(0^{\circ})=1$. Also gilt:

$$\vec{a}\cdot\vec{b} = |\vec{a}|\cdot|\vec{b}| \cdot
\underbrace{\cos(0^{\circ})}_{= 1}.$$

Sind die beiden Vektoren $\vec{a}$ und $\vec{b}$ antiparallel, dann ist der
zwischen ihnen eingeschlossene Winkel $\varphi = \angle(\vec{a},\vec{b}) =
180^{\circ}$ und es gilt $\cos(180^{\circ})=-1$. Damit erhalten wir wiederum aus
der geometrischen Interpreation des Skalarproduktes

$$\vec{a}\cdot\vec{b} = \textcolor{red}{-}|\vec{a}|\cdot|\vec{b}|.$$

## Orthogonalität

In der Geometrie nennt man Geraden **orthogonal**, wenn sie einen rechten Winkel
$\varphi=90^{\circ}$ einschließen. Der Kosinus von $90^{\circ}$ ist aber Null,
also $\cos(90^{\circ})=0$. Damit gilt für die geometrische Interpretation des
Skalarproduktes für die beiden Vektoren $\vec{a}$ und $\vec{b}$:

$$\vec{a}\cdot\vec{b} = |\vec{a}|\cdot|\vec{b}| \cdot
\underbrace{\cos(0^{\circ})}_{= 0} = 0.$$

Wir halten also das folgende **Orthogonalitätskriterium** fest.

```{admonition} Wann sind ... zwei Vektoren orthogonal?
:class: note
Zwei Vektoren $\vec{a}$ und $\vec{b}$ sind genau dann orthogonal, wenn ihr
Skalarprodukt Null ist:

$$\vec{a}\perp\vec{b} \; \Leftrightarrow \; \vec{a}\cdot\vec{b}=0.$$
```

## Senkrechte Projektion eines Vektors auf einen anderen Vektor

Die senkrechte Projektion eines Vektors auf einen anderen Vektor wird häufig in
der Technischen Mechanik benötigt, wenn es darum geht, Kräfte zu zerlegen. Bei
der **senkrechten Projektion** betrachten wir zwei Vektoren $\vec{a}$ und
$\vec{b}$ und lassen beide von demselben Startpunkt $S$ starten. Der Punkt $P$
ist die Pfeilspitze des Vektors $\vec{b}$, also $P = S + \vec{a}$. Wir suchen
dann denjenigen Punkt $L$, so dass die Verbindung von $P$ zu $L$ (also
$\overrightarrow{PL}$) senkrecht auf dem Vektor $\vec{b}$ steht. Diese
Verbindung zwischen $P$ und $L$ wird **Lot** genannt. Der Punkt wird
**Lotfußpunkt** genannt. Oft sagt man umgangssprachlich auch **»das Lot
fällen«**, wenn man den Lotfußpunkt bzw. das Lot konstruiert. Im Kontext der
Vektorrechnung sagt man, man projiziert den Vektor $\vec{b}$ senkrecht auf den
Vektor $\vec{a}$.

Wir wollen nun den Vektor berechnen, der durch senkrechte Projektion von
$\vec{b}$ auf $\vec{a}$ entsteht. Dieser Vektor ist der Verbindungsvektor vom
Startpunkt $S$ zum Lotfußpunkt $L$. Er wird üblicherweise mit

$$\vec{b}_{\vec{a}}$$

bezeichnet. Ohne weitere Berechnungen können wir die Richtung dieses Vektors
angeben, denn es ist die gleiche Richtung wie die des Vektors $\vec{a}$. Wir
wissen daher schon, dass $\vec{b}_{\vec{a}}$ in der Form

$$\vec{b}_{\vec{a}} = x \cdot \frac{\vec{a}}{|\vec{a}|} = x \cdot
\vec{e}_{\vec{a}}$$

dargestellt werden kann. Zur Erinnerung, Richtungen werden normalerweise
normiert, d.h. als Einheitsvektoren angegeben. Wir haben daher den Vektor
$\vec{a}$ noch durch seine Länge $|\vec{a}|$ geteilt und ihn mit
$\vec{e}_{\vec{a}}$ abgekürzt.

Was jetzt noch fehlt ist die Länge des Vektors $x = |\vec{b}_{\vec{a}}|$. Dazu
nutzen wir aus, dass durch das Lot ein rechtwinkliges Dreieck entstanden ist,
für das gilt:

```{math}
:label: chap04sec04eq01
x = \cos(\varphi) \cdot |\vec{b}|.
```

Den Kosinus des eingeschlossenen Winkels $\varphi = \angle(\vec{a},\vec{b})$
können wir wiederum über die geometrische Interpretation des Skalarproduktes
bestimmen. Setzen wir

$$\cos(\varphi) = \frac{\vec{a}\cdot\vec{b}}{|\vec{a}|\cdot|\vec{b}|}$$

in die Gleichung {eq}`chap04sec04eq01` ein, dann erhalten wir

$$x = \cos(\varphi) \cdot |\vec{b}| =
\frac{\vec{a}\cdot\vec{b}}{|\vec{a}|\cdot|\vec{b}|} \cdot |\vec{b}| =
\frac{\vec{a}}{|\vec{a}|}\cdot\vec{b}.$$

Insgesamt lässt sich die senkrechte Projektion $\vec{b}_{\vec{a}}$ des Vektors
$\vec{b}$ auf den Vektor $\vec{a}$ also berechnen als

$$\vec{b}_{\vec{a}} = \left( \frac{\vec{a}}{|\vec{a}|}\cdot\vec{b}\right) \cdot
\vec{e}_{\vec{a}}.$$

Für den senkrecht projizierten Vektor $\vec{b}_{\vec{a}}$ gilt also

$$\vec{b}_{\vec{a}} =
\left(\vec{e}_{\vec{a}}\cdot\vec{b}\right) \cdot \vec{e}_{\vec{a}}.$$

```{admonition} Wie wird die senkrechte Projektion berechnet?
:class: note
Soll die senkrechte Projektion $\vec{b}_{\vec{a}}$ des Vektors $\vec{b}$ auf den
Vektor $\vec{a}$ berechnet werden, normiert man als erstes den Vektor $\vec{a}$:

$$\vec{e}_{\vec{a}} = \frac{\vec{a}}{|\vec{a}|}.$$

Dann berechnet man das Skalarprodukt von dem Einheitsvektor $\vec{e}_{\vec{a}}$
mit $\vec{b}$ und baut den Vektor als

$$\vec{b}_{\vec{a}} = \left(\vec{e}_{\vec{a}} \cdot \vec{b}\right) \cdot
\vec{e}_{\vec{a}}$$

zusammen.
```

## Richtungswinkel und Richtungkosinus

In der geometrischen Interpretation eines Vektors besteht dieser aus einer
Richtung und einer Länge (Betrag). Als nächstes wollen wir die Richtung des
Vektors durch die drei Winkel beschreiben, der Vektor mit den Koordinatenachsen
eines dreidimensionalen kartesischen Koordinatensystems bildet.

Die drei Vektoren, die die Richtungen der drei Koordinatenachsen beschreiben,
nennen wir $\vec{e}_1$, $\vec{e}_2$ und $\vec{e}_3$. In Komponentenschreibweise
lauten sie:

$$\vec{e}_1 = \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}, \quad
\vec{e}_2 = \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix}, \quad
\vec{e}_3 = \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix}, \quad.$$

Der Vektor $\vec{a}$ lautet in Komponentenschreibweise

$$\vec{a}= \begin{pmatrix} a_1 \\ a_2 \\ a_3 \end{pmatrix}$$

und hat die Länge bzw. den Betrag

$$a = |\vec{a}| = \sqrt{a_1^2 + a_2^2 + a_3^2}.$$

Für den eingeschlossenen Winkel $\alpha = \angle(\vec{a},\vec{e}_1)$ des Vektors
$\vec{a}$ mit der 1. Koordinatenachse $\vec{e}_1$ erhalten wir über die
geometrische Interpretation des Skalarproduktes

$$\cos(\alpha) = \frac{\vec{a}\cdot\vec{e}_1}{|\vec{a}|\cdot|\vec{e}_1|} =
\frac{\begin{pmatrix} a_1 \\ a_2 \\ a_3 \end{pmatrix}\cdot
\begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}}{a \cdot 1} = \frac{a_1}{a}.$$

Dieser Wert wird als **Richtungskosinus** von $\vec{a}$ mit der 1.
Koordinatenachse bezeichnet. Wir können nun daraus den **Richtungswinkel**
$\alpha$ berechnen:

$$\alpha = \arccos\left(\frac{a_1}{a}\right).$$

Die gleiche Rechnungen können wir auch für die beiden anderen Koordinatenachsen
durchführen. Insgesamt erhalten wir die folgenden Formeln.

```{admonition} Was sind ... die Richtungswinkel?
:class: note
Die Winkel, die ein Vektor $\vec{a}=(a_1,a_2,a_3)$ mit den Koordinatenachsen
bildet, werden als Richtungswinkel bezeichnet. Sie können über die Formeln

\begin{align*}
\cos(\alpha) &= \frac{a_1}{|\vec{a}|},\\
\cos(\beta)  &= \frac{a_2}{|\vec{a}|},\\
\cos(\gamma) &= \frac{a_3}{|\vec{a}|}
\end{align*}

berechnet werden.
```

## Zusammenfassung und Ausblick

Kollineare und orthogonale Vektoren, speziell die senkrechten
Projektionsvektoren, haben eine große Bedeutung in Physik und Technischer
Mechanik, beispielsweise bei der Zerlegung von Kräften. Auch die Berechnung der
Richtungswinkel hat direkte Anwendungen beispielsweise in der Beschreibung der
Richtung eines Roboterarmes. Daher spielt das Skalarprodukt eine herausrgende
Rolle bei solchen Anwendungen. Speziell für den dreidimensionalen Raum wurde
zusätzlich das Vektorprodukt entwickelt, um weitere Phänomene in Physik und
Technik mathematisch einfach beschreiben zu können. Das Vektorprodukt lernen wir
im nächsten Kapitel kennen.
