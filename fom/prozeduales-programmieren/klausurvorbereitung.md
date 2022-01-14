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




Was ist ein Pointer?
Was ist Pointerarithmetik?
- Rechnen mit Speicheradressen. 
Wofür verwendet man Pointer?

Speicher muss immer freigegeben werden.

ENUM sind nicht Klausurrelevant