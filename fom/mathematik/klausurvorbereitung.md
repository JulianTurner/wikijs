---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-01-13T14:58:38.818Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:44:54.647Z
---

# Klausurvorbereitung

## Grundlagen

Was ist eine Primzahl?
- Eine Primzahl kann man nur durch sich selbst oder 1 teilen z.b. { 3, 5, 7 }
---
### Aussagen

Eine Aussage beinhaltet keine Variable.
- morgen ist Sonntag = keine Aussage da morgen eine Variable ist
- nach Montag kommt Sonntag = aussage
---
### Mengen 
- die leere Menge ist in jeder Menge vorhanden
- eine Schnittmenge ist eine Menge die in der Menge $A$ und $B$ vorhanden ist. 
---
#### Addition von Mengen
$|A \cup B| = |A| + |B| - |A \cap B|$
> Bei Mengen gilt es zu Beachten die Schnittmenge bei Vereinigungen abzuziehen da sie sonst doppelt vorhanden wäre.
---
### Äquivalenzrelationen
---
Was ist reflexsiv?
- Ich habe am slelben Tag Geburtstag wie ich
- $500g \Leftrightarrow 500g$
>  Wenn $x$ in relation zu sich selbst steht
$x \thicksim x$
{.is-info}
---

Was ist symetrisch?
- Ich habe am selben Tag Geburtstag wie mein Zwilling.
- $1/2 kg \Leftrightarrow 500g$
> Wenn $x$ in Relation zu $y$ steht, dann steht $y$ auch in Relation zu $x$
$x \thicksim y \Leftrightarrow y \thicksim x$
{.is-info}
---

Was ist transitiv?
- der zwite drilling hat am selben Tag Geburtstag wie der dritte Drilling und ich habe am selben Tag Geburtstag wie der dritte Drilling.
- $0,5kg \thicksim 1/2 kg \land 1/2 kg \thicksim 500g \implies 0,5kg \thicksim 500g$
> Wenn x in Relation zu $y$ steht ***und*** $y$ in Relation zu $z$, dann steht auch $x$ in Relation zu $z$ 
$x \thicksim y \space \land y\thicksim z \implies x \thicksim z$ 
{.is-info}
---

### Abbildungen

Wann ist eine Abbbildung sujektiv?
- $x:\N, y:={2}$
> Wenn jedes Element in $y$ mindestens 1x getroffen wird
{.is-info}
---

Wann ist eine Abbbildung injektiv?
> Wenn ein Element in $y$ maximal 1x getroffen wird
{.is-info}
---

Wann ist eine Abbbildung bijektiv?
> Wenn die Abbildungeng sowohl sujektiv als auch injektiv ist
{.is-info}
---

# Algebraische Strukturen und Zahlenmengen
---
### Vollständige Induktion
- Beweisen der Bernouli-Ungleichung für $h \in \R$
$\forall n \in \N: {(1+h)^{n}}  \geq 1+nh, falls \space h \geq -1$

Infuktionsanfang: $n = 1$
Rechnung | Rechenschritt
---------|----------
| $(1+h) \geq 1+1*h$ | *Klammern auflösen da nicht benötigt*
| $1+h \geq 1 + 1*h$ | $* 1$ *entfernen*
| $1+h \geq 1 + h$ | $\square$

Induktionsbehauptung
$\exists n \in \N : {{(1+h)^{n}} \geq 1+ nh, falls h \geq -1}$

Induktionsschritt:
- zu zeigen $n \rightarrow n +1$ 
- ${(1+h)^{n+1}} {\geq 1 + (n+1)h}$
- linke Seite so lange umformen und redizieren bis die Ungleichung bewiesen wird


Rechnung | Rechenschritt
---------|----------
${(1+h)^{n+1}}$ | Qutienten aufteilen
$={(1+h)^{n}} * (1+h)$| Induktionsbehauptung einsetzten ${(1+h)^{n}}$ mit $(1+nh)$ ersetzten
$>(1+nh)*(1+h)$ | Klammern ausmultiplizieren
$=1+h+nh+nh^2$| $h$ ausklammern
$=1+h* (1 + n)+nh^2$| umformen 
$=1+(n+1)h +nh^2$| $\square$ siehe unten


$n\in\N = n > 0$
$h^2$ wird immer positiv
Das Ergebnis wird bei einer Addition nicht kleiner

# Kombinatorik ubnd Warscheinlichkeit
Wie viele verschiedene achtstellige Dualzahlen gibt es?
- $2^{8} = 256$	

Wie viele verschiedene achtstellige Dezimalzahlen gibt es?
- $10^{8} = 100000000$

Wie viele Komibantionen aus 3 Buchstaben gibt es in einem Aplphabet $\Sigma={a,b,c}$?
- $3^{3} = 27$

Wie viele Wörter $|w| \geq 3 \vee |w| \leq 5$ aus $\Sigma=\{a,b,c\}$ gibt es?
- $3^3+3^4+3^5$

# Lineare Algebra
$\vec{e} = \left(\begin{array}{c}3 \\ 4 \end{array} \right)$,
$\vec{b} = \left(\begin{array}{c}5 \\ 6 \end{array} \right)$

---

Wie addiert man Vektoren?  

$\vec{c}_eb = {\vec{e} + \vec{b}}$

$\vec{d}_{eb} = \left(\begin{array}{c}3 \\ 4 \end{array} \right) + \left(\begin{array}{c}5 \\ 6 \end{array} \right)$

$\vec{d}_{eb} = \left(\begin{array}{c}8 \\ 10 \end{array} \right)$
> Gleiches gilt auch für Subtraktion
{.is-info}
---

Wie multipliziert man einen Vektor?
$\vec{c}_{me} = {10 * \vec{e}}$

$\vec{c}_{me} = 10* \left(\begin{array}{c}3 \\ 4 \end{array} \right)$

$\vec{c}_{me} = \left(\begin{array}{c}30 \\ 40 \end{array} \right)$
> Gleiches gilt auch für Division
{.is-info}
---

Wie berechnet man die Länge von einem Vektor?
- $\vec{e} = \left(\begin{array}{c}3 \\ 4 \end{array} \right)$ 

- $|| \vec{e} || = \sqrt{3^{2}+4^{2}} = 5$

- $\vec{e}$ hat die Länge $5$

Was ist ein Einheitsvektor?
- der Vektor von einem Vektor, der in die gleiche Richtung zeigt und die Länge $1$ hat.	
- $\frac{1}{Länge\space des \space Vektors} * Vektor$
---
Wie berechnet man den Einheitsvektor?

$\vec{e}_{ev} = {\frac{1}{|| \vec{e} ||} * \vec{e}}$  

$\vec{e}_{ev} = \frac{1}{5}*\left(\begin{array}{c}3 \\ 4 \end{array} \right)$

$\vec{e}_{ev} = \left(\begin{array}{c}\frac{3}{5} \\ \frac{1}{4} \end{array} \right)$


> Die Länge des Einheitsverktors ist $1$
{.is-info}

Was ist ein Gegenvektor?
- der gleiche Vektor nur in anderer Richtung

Wie berechnet man den Gegenvektor?

$\vec{e}_{g} = \vec{e} * (-1)$

$\vec{e}_{g} = \left(\begin{array}{c}3 \\ 4 \end{array} \right) *(-1)$  

$\vec{e}_{g} = \left(\begin{array}{c}-3 \\ -4 \end{array} \right)$

---

Wie berechnet man das Skalarprodukt?  
$\langle e,b \rangle = {\vec{e} * \vec{b}}$

$\langle e,b \rangle = e_1 * b_1 + e_2 * b_2$

$\langle e,b \rangle = 3 * 5 + 4 * 6$

$\langle e,b \rangle = 15 + 24$

$\langle e,b \rangle = 39$

> Wenn das Skalarpordukt 0 ist, dann stehen die Vektoren orthogonal (im rechten Winkel, 90°)
{.is-info}

Wie berechnet man den Winkel zwischen zwei Vektoren?

$cos(\alpha) = {\frac{Skalarprodukt}{||e_1|| * ||e_2||}}$
- Das Ergebnis für $\alpha$ im einsetzten 
- $cos^{-1}$ verwenden
- Der Wert ist in Grad
> Taschenrechner muss aud degree (D) eingestellt sein
{.is-warning}
---

Was ist lineare Unabhängkeit bei Vektoren?
- Mit einem Vektor den anderen Verktor erzeugen
- Ein Vektor ist das vielfache des anderen Vektors

Wie berechnet man linerae unabhängigkeit von Vektoren?  
$\left(\begin{array}{c}3 \\ 4 \end{array} \right) = {r * \left(\begin{array}{c}6 \\ 8 \end{array} \right)}{\begin{cases}
    3 = {r * 6} \xRightarrow{\div3} {r=2}\\
    4 = {r * 8} \xRightarrow{\div4} {r=2}
  \end{cases}
}$

Da $r$ immer gleich ist, ist der Vektor linear abhänging.

> In jeder Zeile muss das gleiche r raus kommen.
{.is-info}