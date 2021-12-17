---
title: Klausurvorbereitung
description: 
published: 1
date: 2021-12-17T09:31:09.552Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:46:52.553Z
---

# Klausurvorbereitung

## Lektion 1: Grundlagen der Graphentheorie

---
S. 14

Woraus besteht ungerichteter Graph $G=(V,E,\varphi)$? 
- einer Menge aus Knoten V
- einer Menge aus Kanten E
- einer Verbindung $\varphi$ zwichen den Knoten
---
S. 14

Was ist der Unterschied zwischen einem einfachen und einem multi Graph?

einfacher Graph:
- $\varphi$ ist injektiv
- ein Paar von Knoten ist höchstens mit einer Kante verbunden

multi Graph:
- $\varphi$ ist nicht injektiv
- ein paar von Knoten ist mit mehreren Kanten **pro Richtung** verbunden 

---
S. 16

Was ist ein Pfad?
- eine Folge von Kanten

Was ist ein Kreis?
- en geschlossener Pfad
- Start und Endknoten identisch

Was ist ein Zyklus?
- Kreis ohne wiederholte Knoten/Kanten

---
S. 17

Was ist ein DAG?
- ein gerichteter Graph ohne Zyklen

Was ist ein Tree?
- ein gerichteter Graph ohne Zyklen
- besitzt eine Wurzel (Root)
- zu jedem Knoten kann nur eine Kante gehen
> In einem gerichteten Baum ist ein Knoten der kein Startpunkt ist ein Blatt (Leaf)

---
S. 19

Was ist ein zusammenhängender Graph?
- ein ungerichteter Graph, heißt zusammenhänged falls zu jedem Knoten eine Kante geht

Was ist ein stark zusammenhängender Graph?
- falls zu jedem Knoten eine Kante geht die auch wieder zurück geht (in beide Richtungen)

---
S. 20

Wann ist ein Graph transitiv abgeschlossen?
- Wenn es zwischen zwei Knoten die <u>über mehrere Kanten verbunden</u> sind, es auch eine Kante gibt welche die Knoten <u>direkt</u> verbindet

Wann ist ein Graph vollständig?
- Wenn es zu jedem Knotenpaar eine Kante gibt

Was ist eine Clique?
- ein Teilgraph der vollständig ist

---
S. 21

Was ist das Kanten Gewicht eines Pfades?
- die Summe aller Kantengewichte

Was ist das Knoten Gewicht eines Pfades?
- die Summe aller Knotengewichte
---

S. 22

Was ist ein bipartit Graph?
- ein Graph, der zwei Teilmengen von Knoten hat
- es gibt nur Katen von einer in die andere Teilmenge
> Bitpartite Graphen werden oft zur Beschreibung von Relationen zwischen zwei Mengen genutzt

---
S. 23

Was ist ein Hamiltonian Pfad?
- ein Pfad, der jeden Knoten genau einmal besucht

Was ist ein Euler Pfad?
- ein Pfad, der jede Kante genau einmal enthält

---
## Lektion 2: Grammatik, reguläre Sprachen und enliche Automaten

---
S. 4

>$\Epsilon$ ist eine Menge an Zeichen (Alphabet)  
>$\Epsilon^+$ ist die Menge aller nicht leeren Zeichenketten  
>$\Epsilon^*$ schließt die leere Zeichenkette $\epsilon$ mit ein  

---
S. 5

Woraus besteht eine Grammatik $G=(V,\Epsilon,P,S)$?
- einer endlichen Menge von Variablen $V$
- einer endlichen Menge von Terminalsymbolen $\Epsilon$
- einer endlichen Menge von Produktionen $P$
- einer startvariable $S$

---
S. 7

### Chomsky Hierarchie

Typ 0:
- es gibt keine Einschränkungen für die Regeln
- erkennbar durch: Turingmaschinen

Typ 1, kontext-sensitiv:
- rechte Seite ist nicht kürzer als linke Seite
- erkennbar durch: erkennbar durch linear bescränkte nicht deterministische Turingmaschinen

Typ 2, kontextfrei:
- die Ersetztung der Variablen ist kontextfrei
- erkennbar durch: nicht deterministischer Kellerautomat

Typ 3, regulär:
- die Ersetzung der Variablen ist regulär
- erkennbar durch: endlicher Automant

---
S. 20

### Endliche Automaten

Woraus besteht ein endlicher Automat $A=(Q,\Epsilon,\delta,q_0,F)$?
- einer Menge an Zuständen $Q$
- einem Alphabet $\Epsilon$
- einer Übergangsfunktion $\delta$
- einem Startzustand $q_0$
- einer Menge an Endzuständen $F$

---
S. 22

Wann erkennt ein endlicher Automat ein Wort?
- wenn es am Ende eines Wortes einen Zustand in der Menge $F$ hat

Wann erkennt ein endlicher Automat ein Wort **nicht**?
- wenn es am Ende eines Wortes keinen Zustand in der Menge $F$ hat
- wenn für das nächte Eingabezeichen kein Zuständsübergang definiert ist

---

Was ist ein deterministischer Automat?
- ein Automat der nur eine Übergangsfunktion für ein ein Termialsymbol hat

---
S. 31

Was ist ein spontaner $\epsilon$ Übergang?
- ein Übergang von einem Zustand zu einem anderen mit einem $\epsilon$ Symbol

>Der Automat kann spontan ohne ein Eingabezeichen zu einem anderen Zustand übergehen

---
### Reguläre Sprachen und reguläre Ausdrücke

S. 35 
>Durch einen DFA akzeptierbare Sprache ist regulär

Sind $a, ß$ reguläre Ausdrücke dann gilt:  | Sprache die einen regulären ausdruck definiert:  
----|-----
$\emptyset$ ist ein regulärer Ausdruck  |$L(\emptyset)= \emptyset$  
$\epsilon$ ist ein regulärer Ausdruck  |$L(\epsilon) = \{ \epsilon \}$  
$a$ ist für jedes $a \in \Sigma$ ein regulärer Ausdruck | $L(a)= \{a\}$  
$aß$ ist ein regulärer Ausdruck |  $L(aß)= L(a)L(b)$  
$a \| ß$ ist ein regulärer Ausdruck |$L(a \| ß)= L(a)\cup L(ß)$
$a^*$ ist ein regulärer Ausdruck |$L(a^*)= L(a)^*$

---
S. 40

Welche Beschreibungsverfahren für reguläre Sprachen sind gleichwertig?
- Reguläre Grammatik
- DFA
- NFA 
- Reguläre Ausdrücke
- EBNF-Grammatik

---
S. 41

Abschlusseigenschaften
- Vereinigung $L_1 \cup L_2$
- Durschschnitt $L_1 \cap L_2$
- Komplement $\bar{L_1} := \Sigma^* \setminus L_1$
- Kleenestern $L^{*}_1 $ 

---
S. 42

#### Pumping Lemma

- jedes Wort hat ein Mittelstück dass sich belieg oft wiederholen lässt ohne die Sprache zu verlassen

---
## Lektion 3: Kentextfreie Sprachen und Push-Down-Automaten

---
S. 5 

### Chomsky Normalform


Eine kontextfrei Grammatik ist in Chomsky Normalform wenn:
- jede Regel ist kontextfrei
- linke Seite besteht aus einer Veriable
- besteht aus einem Terminal oder einer Variable mit Terminalsymbol
- rechte Seite besteht maximal aus 2 Zeichen
- keine $\epsilon$-Regel
- jedes Terminal hat eine Variable

>Kettenregel ist Veriable auf Variable

---
S. 8

###  Greibach Normalform
Eine kontextfrei Grammatik ist in Greibach Normalform wenn:
- jede Regel ist kontextfrei
- linke Seite besteht aus einer Veriable
- rechte Seite beginnt mit einem Terminalsymbol und hat endlich viele Variablen im Anschluss
- keine $\epsilon$-Regel

---

### Charakteristische Merkmale kontextfreier Grammatiken

---
S. 14

Ableitungsbäume
- vereinheitlichten die Auswahl der als nächstes abgeleiteten Variable
- sind für links und rechts Ableitungen identisch

---
S. 15

Wann ist eine kontextfreie Grammatik in mehrdeutig?
- wenn es zu einem Wort verschiedene Ableitungen gibt

---
S. 17

Abschlusseigenschaften kontextfreier Sprachen:
- Vereinigung $L_1 \cup L_2$
- Produkt $L_1 L_2$
- Kleenestern $L^{*}_1 $

---
S. 18

**Nicht**-Abschlusseigenschaften kontextfreier Sprachen:
- Durschschnitt $L_1 \cap L_2$
- Komplement $\bar{L_1} := \Sigma^* \setminus L_1$

---
S. 24

Wofür benötig man den CYK-Algorythmus?
- mit dem CYK-Algorythmus lässt sich feststellen, ob ein Wort zu einer bestimmten kontextfreien Sprache gehört

---
S.28

### Push-Down Automat

Woraus besteht ein Push-Down-Automat $M=(Q,\Sigma,\Gamma,\delta,q_0,\#)$?
- eine Menge an Zuständen $Q$
- einem Alphabet $\Sigma$
- einem Stack-Alphabet $\Gamma$
- einer Übergangsfunktion $\delta$
	- die in Abhängigkeit vom aktuellen Zustand und dem aktuellen Stack-Symbol einen neuen Zustand und einen neuen Stack-Symbol zuweist
- einem Startzustand $q_0$
- einem Anfangssymbol $\# \in \Gamma$
- einer Mengenmenge von Endzuständen *-fehlt im Script* 

> Pda sind in der Regel nicht deterministisch

---
S. 31

Was ist eine Konfiguration eines Push-Down-Automat?
- eine Momentaufnahme des Push-Down-Automat in Arbeit

> Kontextfreie Sprachen sind von einem Push-Down-Automat akzeptierbar

---
S. 41

Folgebde Beschreibungsverfahren für kontextfreie Sprachen sind gleichwertig:

Kontextfreie Grammatik:
- Startsymbol nach $\epsilon$ ist zulässig

Nicht-detereministische Push-Down-Automaten:
- Akzeptieren bei leerem Stack
- Akzeptieren mit Endzustand
- ein oder mehere Startzustände
- ein oder mehere Zustände
- mit und ohne $\epsilon$-Übergänge

---
S. 45

Abschlusseigenschaften deterministisch kontextfreier Sprachen:
- Komplement $\bar{L_1} := \Sigma^* \setminus L_1$

---

Nicht-Abschlusseigenschaften deterministisch kontextfreier Sprachen:
- Durchschnitt $L_1 \cap L_2$
- Vereinigung $L_1 \cup L_2$
## Lektion 4: Kontextsensitive Sprachen, Turingmaschinen
--- 
S. 9

Woraus besteht eine Turnigmaschine $M=(Q,\Sigma,\Gamma,\delta,q_0,\sqcup,F)$?
- eine Menge an Zuständen $Q$
- einem Alphabet $\Sigma$
- einem Arbeits-Alphabet $\Gamma$
- einer Übergangsfunktion $\delta$ welche die Bewegungsrichtung sowie den neuen Zustand
	- unter Abhängigkeit vom 
		- aktuellen Zustand 
		- aktuellen Zeichen 
- einem Startzustand $q_0$
- einem reservierten Blankzeichen $\sqcup \in \Gamma \space \setminus \space \Sigma$
- einer Mengenmenge von Endzuständen $F$

---
S. 12

Was ist eine Konfiguration einer Turingmaschine?
- eine Momentaufnahme der Turingmaschine in Arbeit

> Turingmaschinen können leicht in Endlosschleifen geraten
---
S. 14 

Was macht eine Linear beschränkte Turingmaschine (LBA) aus?
- verlässt nie den Teil des Bandes, auf dem die Eingabe stand
- überschreibt nie ein Blank
- kann so konzepriert werden, dass sie nie ein Blank besucht

> Eine LBA ist eine nicht deterministische Turingmaschine
---
S. 17
Welche Automaten akzeptieren Typ 0 Sprachen?
- Turingmaschinen


Welche Automaten akzeptieren Typ 1 (kontextsensitive Sprachen)?
- LBA

> Eine nicht deterministische Turingmaschine kann durch eine deterministische Turingmaschine simuliert werden

---
S. 20

Was zeichnet eine Mehrband-Turingmaschine aus?
- eine Turingmaschine, die mehrere Bänder hat
- eine Lese-Schreib-Kopf der sich unabhängig von den Bändern bewegt
- eine gemeinsame Zustandsmenge für alle Bänder
- Zustandsübergange werden in Abhängigkeit aller Zeichen auf allen Bändern ausgeführt
- die Schreibköpfe können auf jedem Band etwas anderes schreiben
- die Bewegungsrichtung der Köpf kann auf jedem Band anders sein

> Eine Einband-Turingmaschine ist genso mächtig wie eine Mehrband-Turingmaschine

---
S. 22

Abschlusseigenschaften von Typ 0 Sprachen:
- Vereinigung $L_1 \cup L_2$
- Durchschnitt $L_1 \cap L_2$
- Produkt $L_1 L_2$
- Kleenestern $L^*_1$

Abschlusseigenschaften von Typ 1 Sprachen:
- Vereinigung $L_1 \cup L_2$
- Durchschnitt $L_1 \cap L_2$
- Produkt $L_1 L_2$
- Kleenestern $L^*_1$
- Komplement $\bar{L_1} := \Sigma^* \setminus L_1$
## Lektion 5:

## Lektion 6: