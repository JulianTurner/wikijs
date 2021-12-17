---
title: Klausurvorbereitung
description: 
published: 1
date: 2021-12-16T19:46:52.553Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:46:52.553Z
---

# Klausurvorbereitung

Definitionen von Symbolen


| Bedeutung  | Name     | Symvol    |
| ---------- | -------- | --------- |
| Knoten     | Vertices | Knoten    |
| Kanten     | Edges    | Edges     |
| Verbindung | Phi      | $\varphi$ |

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

Chomsky Hierarchie

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

Endliche Automaten

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
Reguläre Sprachen und reguläre Ausdrücke

S. 35 
>Durch einen DFA akzeptierbare Sprache ist regulär






Sind $a, ß$ reguläre Ausdrücke dann gilt:  | Sprache die einen regulären ausdruck definiert:  
----|-----
$\emptyset$ ist ein regulärer Ausdruck  |$L(\emptyset)= \emptyset$  
$\epsilon$ ist ein regulärer Ausdruck  |$L(\epsilon)= \{\epsilon\}$  
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

Pumping Lemma

- jedes Wort hat ein Mittelstück dass sich belieg oft wiederholen lässt ohne die Sprache zu verlassen

## Lektion 3: Kentextfreie Sprachen und Push-Down-Automaten



## Lektion 4:

## Lektion 5:

## Lektion 6: