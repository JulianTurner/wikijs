---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-01-13T19:25:58.309Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:44:54.647Z
---

# Klausurvorbereitung

## Grundlagen

Was ist eine Primzahl?
- Eine Primzahl kann man nur durch sich selbst oder 1 teilen z.b. { 3, 5, 7 }
&zwnj; 
---
### Aussagen

Eine Aussage beinhaltet keine Variable.
- morgen ist Sonntag = keine Aussage da morgen eine Variable ist
- nach Montag kommt Sonntag = aussage
&zwnj; 
---
### Mengen 
- die leere Menge ist in jeder Menge vorhanden
- eine Schnittmenge ist eine Menge die in der Menge $A$ und $B$ vorhanden ist. 
&zwnj; 
---
#### Addition von Mengen
$|A \cup B| = {|A| + |B| - |A \cap B|}$
Bei Mengen gilt es zu Beachten die Schnittmenge bei Vereinigungen abzuziehen da sie sonst doppelt vorhanden wäre.&zwnj; 

---
### Äquivalenzrelationen
Was ist reflexsiv?
- Ich habe am slelben Tag Geburtstag wie ich
- ${500g \Leftrightarrow 500g}$
Wenn $x$ in relation zu sich selbst steht
${x \thicksim x}$
&zwnj; 

Was ist symetrisch?
- Ich habe am selben Tag Geburtstag wie mein Zwilling.
- $1/2 kg \Leftrightarrow 500g$
Wenn $x$ in Relation zu $y$ steht, dann steht $y$ auch in Relation zu $x$
- $x \thicksim y \Leftrightarrow y \thicksim x$
&zwnj; 
---

Was ist transitiv?
- der zwite drilling hat am selben Tag Geburtstag wie der dritte Drilling und ich habe am selben Tag Geburtstag wie der dritte Drilling.
- ${0,5kg \thicksim 1/2 kg \land 1/2 kg \thicksim 500g \implies 0,5kg \thicksim 500g}$
Wenn x in Relation zu $y$ steht ***und*** $y$ in Relation zu $z$, dann steht auch $x$ in Relation zu $z$ 
- ${x \thicksim y \space \land y\thicksim z \implies x \thicksim z}$ 
&zwnj; 
---

### Abbildungen

Wann ist eine Abbbildung sujektiv?
- ${x:\N, y:=2}$ &zwnj;
- Wenn jedes Element in $y$ mindestens 1x getroffen wird &zwnj;
&zwnj; 
---

Wann ist eine Abbbildung injektiv?
- Wenn ein Element in $y$ maximal 1x getroffen wird &zwnj; 

---

Wann ist eine Abbbildung bijektiv?
- Wenn die Abbildungeng sowohl sujektiv als auch injektiv ist &zwnj; 

---

# Algebraische Strukturen und Zahlenmengen
---
### Vollständige Induktion
- Beweisen der Bernouli-Ungleichung für ${h \in \R}$ &zwnj;

$\forall n \in \N:(1+h)^{n}  \geq 1+nh, falls \space h \geq -1$ &zwnj;


Infuktionsanfang: $n = 1$ &zwnj;

Rechnung | Rechenschritt
---------|----------
${(1+h) \geq 1+1*h}$ &zwnj; | *Klammern auflösen da nicht benötigt*
${1+h \geq 1 + 1*h}$ &zwnj;| ${* 1}$ *entfernen*
${1+h \geq 1 + h}$ &zwnj;| ${\square}$&zwnj;

&zwnj; 
Induktionsbehauptung
${\exists n \in \N : (1+h)^{n} \geq 1+ nh, falls h \geq -1}$
&zwnj; 
Induktionsschritt:
- zu zeigen $n \rightarrow n +1$ 
&zwnj; 
- $(1+h)^{n+1} \geq 1 + (n+1)h$
&zwnj; 
- linke Seite so lange umformen und redizieren bis die Ungleichung bewiesen wird
&zwnj; 

Rechnung | Rechenschritt
---------|----------
$(1+h)^{n+1}$ &zwnj;| Qutienten aufteilen
$=(1+h)^{n} * (1+h)$ &zwnj;| Induktionsbehauptung einsetzten $(1+h)^{n}$ mit $(1+nh)$ ersetzten
$>(1+nh)*(1+h)$ &zwnj;| Klammern ausmultiplizieren
$=1+h+nh+nh^2$ &zwnj;| $h$ ausklammern 
$=1+h* (1 + n)+nh^2$ &zwnj;| umformen  
$=1+(n+1)h +nh^2$ &zwnj;| $\square$ siehe unten

&zwnj; 

$n\in\N = n > 0$
&zwnj; 
$h^2$ wird immer positiv
Das Ergebnis wird bei einer Addition nicht kleiner

# Kombinatorik ubnd Warscheinlichkeit
Wie viele verschiedene achtstellige Dualzahlen gibt es?
- $2^{8} = 256$	
&zwnj; 
Wie viele verschiedene achtstellige Dezimalzahlen gibt es?
- $10^{8} = 100000000$
&zwnj; 
Wie viele Komibantionen aus 3 Buchstaben gibt es in einem Aplphabet $\Sigma={a,b,c}$?
- $3^{3} = 27$
&zwnj; 
Wie viele Wörter $|w| \geq 3 \vee |w| \leq 5$ aus $\Sigma=\{a,b,c\}$ gibt es?
- $3^3+3^4+3^5$
&zwnj; 
# Lineare Algebra

## Vektoren
---
gegeben:
$\vec{e} = \left(\begin{array}{c}3 \\ 4 \end{array} \right)$,
&zwnj; 
$\vec{b} = \left(\begin{array}{c}5 \\ 6 \end{array} \right)$
&zwnj; 
---

Wie addiert man Vektoren?  

$\vec{c}_eb = {\vec{e} + \vec{b}}$
&zwnj; 
$\vec{d}_{eb} = \left(\begin{array}{c}3 \\ 4 \end{array} \right) + \left(\begin{array}{c}5 \\ 6 \end{array} \right)$
&zwnj; 
$\vec{d}_{eb} = \left(\begin{array}{c}8 \\ 10 \end{array} \right)$
&zwnj; 
> Gleiches gilt auch für Subtraktion
{.is-info}
---

Wie multipliziert man einen Vektor?
$\vec{c}_{me} = {10 * \vec{e}}$
&zwnj; 
$\vec{c}_{me} = 10* \left(\begin{array}{c}3 \\ 4 \end{array} \right)$
&zwnj; 
$\vec{c}_{me} = \left(\begin{array}{c}30 \\ 40 \end{array} \right)$
&zwnj; 
> Gleiches gilt auch für Division
{.is-info}
---

Wie berechnet man die Länge von einem Vektor?
- $\vec{e} = \left(\begin{array}{c}3 \\ 4 \end{array} \right)$ 
&zwnj; 
- $|| \vec{e} || = \sqrt{3^{2}+4^{2}} = 5$
&zwnj; 
- $\vec{e}$ hat die Länge $5$
&zwnj; 
Was ist ein Einheitsvektor?
- der Vektor von einem Vektor, der in die gleiche Richtung zeigt und die Länge $1$ hat.	
- $\frac{1}{Länge\space des \space Vektors} * Vektor$
---
Wie berechnet man den Einheitsvektor?

$\vec{e}_{ev} = {\frac{1}{|| \vec{e} ||} * \vec{e}}$  
&zwnj; 
$\vec{e}_{ev} = \frac{1}{5}*\left(\begin{array}{c}3 \\ 4 \end{array} \right)$
&zwnj; 
$\vec{e}_{ev} = \left(\begin{array}{c}\frac{3}{5} \\ \frac{1}{4} \end{array} \right)$
&zwnj; 

> Die Länge des Einheitsverktors ist $1$
{.is-info}
&zwnj; 
Was ist ein Gegenvektor?
- der gleiche Vektor nur in anderer Richtung

Wie berechnet man den Gegenvektor?

$\vec{e}_{g} = {\vec{e} * (-1)}$
&zwnj; 
$\vec{e}_{g} = {\left(\begin{array}{c}3 \\ 4 \end{array} \right) *(-1)}$  
&zwnj; 
$\vec{e}_{g} = {\left(\begin{array}{c}-3 \\ -4 \end{array} \right)}$
&zwnj; 
---

Wie berechnet man das Skalarprodukt?  
$\langle e,b \rangle = {\vec{e} * \vec{b}}$
&zwnj; 
$\langle e,b \rangle = {e_1 * b_1 + e_2 * b_2}$
&zwnj; 
$\langle e,b \rangle = {3 * 5 + 4 * 6}$
&zwnj; 
$\langle e,b \rangle = {15 + 24}$ 
&zwnj; 
$\langle e,b \rangle = {39}$  
&zwnj; 
> Wenn das Skalarpordukt 0 ist, dann stehen die Vektoren orthogonal (im rechten Winkel, 90°)

---
Wie berechnet man den Winkel zwischen zwei Vektoren?

$cos(\alpha) = {\frac{Skalarprodukt}{||e_1|| * ||e_2||}}$
&zwnj; 
- Das Ergebnis für $\alpha$ im einsetzten 
- $cos^{-1}$ verwenden
- Der Wert ist in Grad
> Taschenrechner muss aud degree (D) eingestellt sein
{.is-warning}
---

Was ist lineare Unabhängkeit bei Vektoren?
- Mit einem Vektor den anderen Verktor erzeugen
- Ein Vektor ist das vielfache des anderen Vektors
---

Wie berechnet man linerae unabhängigkeit von Vektoren?  

$\left(\begin{array}{c}3 \\ 4 \end{array} \right) = {r * \left(\begin{array}{c}6 \\ 8 \end{array} \right)}{\begin{cases}
    3 = {r * 6} \xRightarrow{\div3} {r=2}\\
    4 = {r * 8} \xRightarrow{\div4} {r=2}
  \end{cases}
}$
&zwnj; 
Da $r$ immer gleich ist, ist der Vektor linear abhänging.

> In jeder Zeile muss das gleiche r raus kommen.
{.is-info}
---

## Matrizen
gegeben:
$A1=\left(\begin{array}{cc}
	1 & 2 \\
	3 & 4 \end{array} \right)$
&zwnj; 
$A2=\left(\begin{array}{cc}
	3 & 4 \\
	5 & 6 \end{array} \right)$
&zwnj; 
$A3=\left(\begin{array}{cc}
	3 & 4 \\
	5 & 6 \\
	1 & 2\end{array} \right)$
&zwnj; 
$A4=\left(\begin{array}{cc}
	6 & 8 & 3 \\
	4 & 7 & 3\\
	1 & 2 & 1\end{array} \right)$
&zwnj; 
### Matrix transponieren
Wie transponiert man eine Matrix?
<p><a href="https://commons.wikimedia.org/wiki/File:Matrix_transpose.gif#/media/Datei:Matrix_transpose.gif"><img src="https://upload.wikimedia.org/wikipedia/commons/e/e4/Matrix_transpose.gif" alt="Matrix transpose.gif"></a><br>Von &lt;a href="//commons.wikimedia.org/wiki/User:LucasVB" title="User:LucasVB"&gt;Lucas Vieira&lt;/a&gt; - &lt;span class="int-own-work" lang="de"&gt;Eigenes Werk&lt;/span&gt;, Gemeinfrei, <a href="https://commons.wikimedia.org/w/index.php?curid=21897854">Link</a></p>

$A1^T = \left(\begin{array}{cc}
	1 & 2 \\
	3 & 4 \end{array} \right)$
&zwnj;
$A3^T=\left(\begin{array}{cc}
	3 & 5 & 1 \\
	4 & 6 & 2 
	\end{array} \right)$

### Was ist eine Einheitsmatrix?
- Eine Matrix bei der die Diagonale aus 1 besteht, und der Rest nur aus 0

$AE=\left(\begin{array}{cc}
	1 & 0 & 0 \\
	0 & 1 & 0\\
	0 & 0 & 1\end{array} \right)$
&zwnj; 

---

### ### Inverse einer Matrix mit dem Gauß-Jordan-Verfahren
#### Einheitsmatrix neben die Matrix schreiben

$A4=\left(\begin{array}{cc}
	6 & 8 & 3 \\
	4 & 7 & 3\\
	1 & 2 & 1\end{array} \right)
\left(\begin{array}{cc}
	1 & 0 & 0 \\
	0 & 1 & 0\\
	0 & 0 & 1\end{array} \right)$
&zwnj;

#### linke Seite zur Einheitsmatrix umformen und die Schritte auf beide Matrizen anwenden

**1. Oben Links eine 1 in der Diagonale**

$A4=\left(\begin{array}{cc}
	\color{red}1 & \color{grey}X & \color{grey}X \\
	\color{grey}X & \color{grey}X & \color{grey}X\\
	\color{grey}X & \color{grey}X & \color{grey}X\end{array} \right)$
&zwnj;

- Erste Zeite mit der dritten Zeile vertauschen

$A4=\left(\begin{array}{cc}
	1 & 2 & 1 \\
	4 & 7 & 3\\
	6 & 8 & 3\end{array} \right)
	\left(\begin{array}{cc}
	0 & 0 & 1 \\
	0 & 1 & 0\\
	1 & 0 & 0\end{array} \right)$

**2. Erste Spalte mit 0 auffüllen**

$A4=\left(\begin{array}{cc}
	1 & \color{grey}X & \color{grey}X \\
	\color{red}0 & \color{grey}X & \color{grey}X\\
	\color{red}0 & \color{grey}X & \color{grey}X\end{array} \right)$
&zwnj;

- da die erste Spalte 1 ist, kann man $Zeile 2 - 4 x Zeile 1$

$A4=\left(\begin{array}{cc}
	1 & 2 & 1 \\
	0 & -1 & -1\\
	6 & 8 & 3\end{array} \right)
	\left(\begin{array}{cc}
	0 & 0 & 1 \\
	0 & 1 & -4\\
	1 & 0 & 0\end{array} \right)$


- da die erste Spalte 1 ist, kann man $Zeile 3 - 6 x Zeile 1$

$A4=\left(\begin{array}{cc}
	1 & 2 & 1 \\
	0 & -1 & -1\\
	0 & -4 & -3\end{array} \right)
	\left(\begin{array}{cc}
	0 & 0 & 1 \\
	0 & 1 & -4\\
	1 & 0 & -6\end{array} \right)$


**3. Zweite Zeile zweilte Spalte eine 1**

$A4=\left(\begin{array}{cc}
	1 & \color{grey}X & \color{grey}X \\
	0 & \color{red}1 & \color{grey}X\\
	0 & \color{grey}X & \color{grey}X\end{array} \right)$
&zwnj;

- zweite zeile mit $(-1)$ multiplizieren (das dreht alle Vorzeichen um)

$A4=\left(\begin{array}{cc}
	1 & 2 & 1 \\
	0 & 1 & 1\\
	0 & -4 & -3\end{array} \right)
	\left(\begin{array}{cc}
	0 & 0 & 1 \\
	0 & -1 & 4\\
	1 & 0 & -6\end{array} \right)$

**4. Dritte Zeile zweilte Spalte eine 0**

$A4=\left(\begin{array}{cc}
	1 & \color{grey}X & \color{grey}X \\
	0 & 1 & \color{grey}X\\
	0 & \color{red}0 & \color{grey}X\end{array} \right)$
&zwnj;

- Zeile 3 mit 4x Zeile 2 addieren

$A4=\left(\begin{array}{cc}
	1 & 2 & 1 \\
	0 & 1 & 1\\
	0 & 0 & 1\end{array} \right)
	\left(\begin{array}{cc}
	0 & 0 & 1 \\
	0 & -1 & 4\\
	1 & -4 & 10\end{array} \right)$

**5. Dritte Zeile dritte Spalte eine 1** 

$A4=\left(\begin{array}{cc}
	1 & \color{grey}X & \color{grey}X \\
	0 & 1 & \color{grey}X\\
	0 & 0 & \color{red}1\end{array} \right)$
&zwnj;

- Nicht notwendig da schon vorhanden. Ansonsten durch einfach durch den Wert teilen.

**6. Dritte Zeile und zweite Zeile dritte Spalte eine 0** 

$A4=\left(\begin{array}{cc}
	1 & \color{grey}X & \color{red}0 \\
	0 & 1 & \color{red}0\\
	0 & 0 & 1\end{array} \right)$
&zwnj;

- Da dritte Zeile nur 0 in der ersten und zweiten Spalte hat wird sie jetzt von der Zeile 1 und 2 abgezogen.

$A4=\left(\begin{array}{cc}
	1 & 2 & 0 \\
	0 & 1 & 0\\
	0 & 0 & 1\end{array} \right)
	\left(\begin{array}{cc}
	-1 & 4 & -9 \\
	-1 & 3 & -6\\
	1 & -4 & 10\end{array} \right)$

**7. Erste Zeile zweite Spalte eine 0** 

$A4=\left(\begin{array}{cc}
	1 & \color{red}0 & 0 \\
	0 & 1 & 0\\
	0 & 0 & 1\end{array} \right)$
&zwnj;

- die Zeile 1 - 2 x Zeile 2 

$A4=\left(\begin{array}{cc}
	1 & 0 & 0 \\
	0 & 1 & 0\\
	0 & 0 & 1\end{array} \right)
	\left(\begin{array}{cc}
	1 & -2 & 3 \\
	-1 & 3 & -6\\
	1 & -4 & 10\end{array} \right)$

- fertig

$A^{-1}=\left(\begin{array}{cc}
	1 & -2 & 3 \\
	-1 & 3 & -6\\
	1 & -4 & 10\end{array} \right)$

---

### Matrixmultiplikation

Vorraussetzung:
- Spalten der Matrix 1 = Zeilen der Matrix 2
Ergebis:
- Eine Matrix mit der Höhe von Matrix 1 und einer Breite von Matrix 2
Rechenweg:
- Das erste Element mit einander multiplizieren + die Multiplikation der zweiten Elemente

$
A3=\left(\begin{array}{cc}
	3 & 4 \\
	5 & 6 \\
	1 & 2\end{array} \right)
*
A1=\left(\begin{array}{cc}
	1 & 2 \\
	3 & 4 \end{array} \right)	
$
&zwnj; 

Rechnungen:

- Matrix 1 Reihe 1, Matrix 2 Spalte 1:  
$3*1+4*3=15$  
- Matrix 1 Reihe 2, Matrix 2 Spalte 1:   
$5*1+6*3=23$  
- Matrix 1 Reihe 3, Matrix 2 Spalte 1:  
$1*1+2*3=7$  
&zwnj; 

- Matrix 1 Reihe 1, Matrix 2 Spalte 2:  
$4*1+4*3=16$  
- Matrix 1 Reihe 2, Matrix 2 Spalte 2:  
$6*1+6*3=24$  
- Matrix 1 Reihe 3, Matrix 2 Spalte 2:  
$2*1+2*3=8$  
&zwnj; 

$A_{12}=\left(\begin{array}{cc}
	15 & 16 \\
	23 & 24 \\
	7 & 8 \end{array} \right)	
$
&zwnj; 

## Folgen und Reihen
### Quotientenkriterium
1. Qutienten bilden
	- Nenner k
	- Zähler k + 1
2. Betrag bilden
3. Grenzwert berechnen

- Das Ergbnis ist eine Kennzahl

Kennzahl | Bedeutung
---------|----------
$< 1$ &zwnj;| konvergiert (es kommt ein endlicher Wert raus)
$> 1$ &zwnj;| devergiert (es kommt kein endlicher Wert raus)
$= 1$ &zwnj;| man kann keine Aussage treffen

### Wurzelkriterium
1. Betrag bilden
2. k Wurzel zeihen 
3. Grenzwert berechnen

- Das Ergbnis ist eine Kennzahl

Kennzahl | Bedeutung
---------|----------
$< 1$ &zwnj;| konvergiert (es kommt ein endlicher Wert raus)
$> 1$ &zwnj;| devergiert (es kommt kein endlicher Wert raus)
$= 1$ &zwnj;| man kann keine Aussage treffen


> Jede Reihe die mit Quotientenkriterium berechnet werden kann, kann auch mit dem Wurzelkriterium berechnet werden. Anders herum aber nicht.
.{is-info}
# Elementare Funktionen und Stetigkeit
### Verknüpfung von Funktionen
$f(x)=2x$,  
&zwnj;
$g(x)=x^{2}$  
&zwnj;  
$f \circ g(x) = f ( g (x))$    
&zwnj;  
$f ( g (x)) = f (x^{2})$  
	&zwnj;
$f (x^{2}) = 2* x^{2}$
 
# Differentalrechnung
### Ableitungsregeln

#### Konstanten
- Kontstante fällt weg  

$f(x)=2$
$f'(x)=0$	
&zwnj;
#### Ableitung von $x$
- Ableitung von $x$ ist $1$  

$f(x)=x$  
$f'(x)=1$  
&zwnj;
#### Potenzregel
- Exponent nach vorne holen und im Exponenten um 1 verringern 

$f(x)=x^{n}$  
$f'(x)=nx^{n-1}$  
&zwnj;
#### Faktorregel
- der Faktor bleibt erhalten 

$f(x)=t*x^{n}$  
$f'(x)=n*t*x^{n-1}$  
&zwnj;

#### Summenregel & Differenzregel
- Jeder Teil wird einzeln abgeleitet  

$f(x)=x^{n} + x^{m}$   
$f'(x)= n * x^{n-1} + m * x^{m-1}$  
&zwnj;

#### Produktregel
- Teile aufsplitten

$f(x)=x^{n} * x^{m}$   
$u = x^{n}$  
$u'= n * x^{n -1}$   
$v = x^{m}$  
$v'= m * x^{m -1}$   
$f'(x)= u' * v + u * v'$
&zwnj;
#### Quotientenregel
- Teile aufsplitten  

$f(x)=\frac{x^{n}}{x^{m}}$  
$u = x^{n}$   
$u'= n * x^{n -1}$   
$v = x^{m}$  
$v'= m * x^{m -1}$  
$f'(x)=\frac{u'*v - v' * u}{v^{2}}$  
&zwnj;
#### Kettenregel
- Teile aufsplitten  

$f(x)=(x^n + 5)^{m}$     
$u = x^{n} + 5$  
$u'= n * x^{n -1}$    
$v= (u)^m$    
$v'= m * (u)^{m-1}$
$f'(x) = u' v'
### Extrema und Wendepunkt

# Integralrechnung
### Stammfunktion
### partielle Integration
### Substitutionsmethode

# Funktionen mehrerer Variablen
### Gradienten bestimmen
### Ableitungen bestimmen
### Extrema und Wendepunkt
