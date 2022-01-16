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

## Teil 2:

Was ist eine Programierrsprache?
- eine formale Sprache
- beschreiben Algorithmen die auf einer Maschine ausgeführt werdwen
- Schnittstelle zwischen Programmierer und Maschine 
---

Was ist Hardware?
- eine fest installierte physische Grundlage 


Was ist Software?
- bestimmt welche Aufgaben auf der Hardware ausgeführt werden

Was ist der Vorteil von der Aufspalung von Hardware und Software?
---

Was zeichnet eine vnn Neumann-Architektur aus?
- eine Rechnerarchitektur die Zentaleinheit und Hauptspeicher trennt 
- der Hauptspeicher enthält Daten auf dem ein Programm operiert, und das Programm selbst
- den Flaschenhals da die ALU und die Steuerung der Zentraleinheit konkurierend auf den Speicher zugreifen
---

Was ist eine Turingmaschine?
- ein theoretisches Konstrukt
- für Lösung eines mathematischen Problems
- Reduziert in den Anforderng
- kleinste Möglichkeit zur Berechnung
- kann jeden Algorythmus der in endlicher Zeit berechnet werden kann, berechnen
- wenn es ein Computer ausrechnen kann, kann es die Turingmaschine auch

Wie schreibt Turingmaschine auf das Band?
- Je nach aktuellen Zustand und Zeichen welches gelsen wurde, bewegt sich die Turingmaschine in 
eine in der Übrgangsfunktion definierte Richtung, und schreibt den Buchstaben welcher in der Übergangsfunktion steht auf das Band.
---


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
	- eval (meta programmierung)
	- objektsysteme zur laufzeit veränderbar
	- duck typing (keine scharfe typüberprüfung)
	- reflexion (fähigkeit informationen über sich selbst zu bekommen)

## Algorithmen
- kurz
- präzise
- eindeutig

Was ist ein Algorithmus?
- eine endliche Menge von konkreten Anweisungen, die ein bestimmtes Problem lösen,

Welche Ablaufstrukturen gibt es?
- reihung
- verzweigung
- wiederholung

Was ist eine Datenstuktur?
Welche Teile gehören zu einer Datenstruktur?
Benötigt ein Algorithmus eine bestimmte Datenstruktur?

- die beste organisation von daten gibt es nicht

Was ist ein Programm?
- besteht aus datenstrukturen
- besteht aus algoritmen
- ist auf einem computer lauffährig

Welche aufgabe erfüllt der präprozessor?
Erläutern sie die fulktionen des präprozessor

Welche arten von fehlern können ein compiler zurück liefern?
Welche Aufgabe übernimmt ein linker?

Welche Variablennamen sind gültig?
Übertragen sie Variablen in snakecase usw

In welcher Reinfolge werden die Abkürzungen genutzt?

Was ist ein casting?
Wofür benötige ich einen casting?
Beipsiel von casting

Platzhalter kennen

Schaltjahr aufgabe sollte man können
Erläuertn sie den Untsfchied zwischen while oder schleife 
Erläutern sie die Aufgabe von break
Übung 11 

Was ist ein Stellenwert system?
Erkennen von Hex werten

Warum hat int ein Wertberech?
Warum hat signed int einen asymmetrisch wertbereich?

Was ist ein Byte?
Umgang mit Einheiten

Was ist ein Short-Curcuit/Kurzschlussoperator?
Warum sollte man keine gleitkommerzahlen miteinander vergleichen?
durch ungenauigkeiten in rechnungen
float zahlen haben nur eine endliche genauikgeit
da nach jedem rechnschritt in das float gekürzt wird und rundugsfehler entsthehen
lösung wäre eine tolerranz von abweichungen

Nullbyte verschieben können
Wass passiert wenn ich kein Nullbyte habe?
chomp funktion anwenden
2 String zusammen fügen
Strings zerlegen
String an einem bestimmten Zeichen zerlegen

Was ist ein Stack?
Wie funktioniert ein Stack?
Was ist eine auto variable?
Was hat das mit dem Stack zu tun?
Was haben funktionen mit einem Stack zu tun?

Was können sie machen wenn sie mehrere Werte einer funktion zurück gben möchten?
Was ist der untschied zwischen der übergabd der kopie und referenz?
Was ist ein buffer overflow?
Wie geht eine funktion ohne rückgabe?
was verstewht man unter rekursion?
was versteht man unter einem pointer?
was versteht man unter einem nullpointer?

formen sie array notation zu pointernotation?

benutzen sie malloc und free
Wann brauche ich malloc und free






Was ist ein Pointer?
Was ist Pointerarithmetik?
- Rechnen mit Speicheradressen. 
Wofür verwendet man Pointer?

Speicher muss immer freigegeben werden.

ENUM sind nicht Klausurrelevant