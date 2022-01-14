---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-01-08T07:43:10.002Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:53:06.780Z
---

# Klausurvorbereitung

Teil 2:
Was ist Hardware?
Was ist Software?
Was ist der Vorteil von der Aufspalung von Hardware und Software?
Was ist Van Neumann-Architektur?
Was ist eine Turingmaschine?
- Ist ein geadnken Experiment
- für lösung eines mathematischen Problems
- Reduziert in den Anforderng
- kleinste Möglichkeit zur Berechnung
- kann jeden Algorythmus der in endlicher zeit berechnet werden kann, berechnen
- wenn es ein computer ausrechnen kann, kann es die turingmaschine auch

was schreiben sie aufs band?
in welchem Zustand bedinden sie sich?
in welche Richtung gehe ich?

Was bedeuted speicherprogrammiert?
Woher holt sich der Prozessor seine Anweisungen?
Welche Sprache versteht ein Prozessor nattiv?
Maschienensprache
Wofür ist das Anfällig?
- programmierfehler
- schwer zu debuggen
Wie wurder das vereinfacht?
- mit dem Assembler
Assembler ist eine schöberer Schreibweise für ein Maschienensprache
Assemblercodes sind von Prozessor zu Prozessor unterschiedlich
Schwierigkeiten mit dem Assembler
- zeitaufwendig
- fehleranfällig
- maximale Maschienennähe => maximale Problemferne

Was macht eine Hochsprache?
- Abstrahiert Assembler in eine Sprache die Näher an der Menschliichen Sprache ist

Was ist die Aufgabe eines Compilers?
- Quellcode in Maschienensprache zu übersetzten?

Wie ist ein Compiler aufgebaut?
3 Gliedrig

Front End
- analysiert Quellcode
- erzeugt eine symantisch äquvivalente Darstekkung Form eines Zwischencodes

Middle End
- kann mit den Frontend-Daten arbeiten und optimierung vornehmen

Backbend
- erzeugt die Maschienensprache
- abhänig von Zielhardware

Was muss bei einer neuen CPU passieren?
- neues Backend

Was benötigt man für eine neue Programmiersprach?
- neues Frontend

Was passiert im frontend?
- lexikanische analyse
- preprocessing
- syntaxanalyse
- semantische analyse

Was passiert im middleend?
- inlline expansion
- dead code elemination
- constant folding
- loop optimization
- automatische parallelisierung

Was passiert im backend?
- erzeugen des maschienencodes
- kann für eine zielplattform optimieren

Wofür sorgen interpreter?
- führen dan übersetzter und die berechnungen durch
- ursprünglich für kleine programme gedacht

Was ist meta programmierung?
- code generator
- erzeugt ein Programm in einer programmiersprache

Was ist der vorteil von virtuellen prozessoren?
- code wird für diesen bestimmten code compiliert

Was ist der Nachteil von virtuellen prozessoren?
- braucht eine zwischenschicht(virtuelle maschine) zum echten prozessor

Wofür brauche ich einen debugger?
- steuerung des programm laufs
- inspektion des zustand zu jedem zeitpunkt


## Programmierparadigmen

Wie unterteilen sich programmiersprachen?
- systemorientierte sprachen
- problemorientierte sprachen

Wie unterteilen sich systemorientierte sprachen?
- maschienensprache
- assembler

Wie unterteilen sich problemorientierte sprachen?
- imperative sprachen
- declarativer sprachen

Wie unterteilen sich imperative sprachen?
- strukturierte sprachen
- prozedale sprachen
- objektorientierte sprachen

Wie unterteilen sich deklarativer sprachen?
- logische sprachen
- funktionale sprachen

Welche elemente hate eine strukturierte sprache?

### Objektorientierte Programiersprachen

Welche konzepte von objektorientierter sprache gibt es?
- strukturierte daten und funktionen
- sprachkonzepte
	- vererbung
	- kapselung
	- polymorphie (mehr förmig)
- in der regel prozedural
- grundlage für kompenetenbasierte entwicklung


### Funktionale Programiersprachen
- bestehen aus funktionen im mathematischen sinne
- sind durch rekursion enebnso mächtig wie imperative oder objektorientierte sprachen
- funktionen haben keine Seiteneffekte
- lassen sich gut parallelisieren
- bestimmt probkleme lassen sich mit wenig code lösen
- ungeeignet für andere sachen


### dynamische Programiersprachen
- keine scharfe abgrenzung
- führen tätigkeiten zur laufzeit aus
- dynamisch typisiert
- typische eigenschaften
	- automatische speicherverwaltung
	- eval
	- objektsysteme zur laufzeit veränderbar
	- duck typing
	- reflexion
	- cloures
	- interne dsl



Was ist ein Pointer?
Was ist Pointerarithmetik?
- Rechnen mit Speicheradressen. 
Wofür verwendet man Pointer?

Speicher muss immer freigegeben werden.

ENUM sind nicht Klausurrelevant