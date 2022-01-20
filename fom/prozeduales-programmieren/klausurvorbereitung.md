---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-01-20T18:34:52.585Z
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

Was zeichnet eine von Neumann-Architektur aus?
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


Was bedeuted Speicherprogrammiert?
- umsetzung der Programmlogik erfolgt Hardware unabhängig

Woher holt sich der Prozessor seine Anweisungen?
- aus dem Speicher

Welche Sprache versteht ein Prozessor nattiv?
- Maschienensprache 

#### Maschienensprache
Wofür ist das Anfällig?
- programmierfehler
- schwer zu debuggen

Wie wurder das vereinfacht?
- mit dem Assembler
- Assembler ist eine schöberer Schreibweise für ein Maschienensprache.
- Assemblercodes sind von Prozessor zu Prozessor unterschiedlich.

Was sind die Schwierigkeiten mit dem Assembler?
- zeitaufwendig
- fehleranfällig
- maximale Maschienennähe => maximale Problemferne

Was macht eine Hochsprache?
- Abstrahiert Assembler in eine Sprache die Näher an der menschliichen Sprache ist

Was ist die Aufgabe eines Compilers?
- Quellcode in Maschienensprache zu übersetzten

Wie ist ein Compiler aufgebaut?
3 Gliedrig

Front End
- analysiert Quellcode
- erzeugt eine symantisch äquvivalente Darstellung in Form eines Zwischencodes

Middle End
- kann mit den Frontend-Daten arbeiten und optimierung vornehmen

Back End
- erzeugt die Maschienensprache
- abhänig von Zielhardware

Was muss bei einer neuen CPU passieren?
- neues Backend

Was benötigt man für eine neue Programmiersprache?
- neues Front End

Was passiert im Front End?
- lexikanische Analyse
- preprocessing
- syntaxanalyse
- semantische analyse

Was passiert im Middle End?
- inlline expansion 
- dead code elemination
- constant folding
- loop optimization
- automatische parallelisierung

Was passiert im Back End?
- erzeugen des Maschienencodes
- kann für eine Zielplattform optimieren

Wofür sorgen Interpreter?
- führen den Übersetzter und die Berechnungen durch
- ursprünglich für kleine Programme gedacht

Was ist Meta Programmierung?
- Code Generator
- erzeugt ein Programm in einer Programmiersprache

Was ist der Vorteil von virtuellen Prozessoren?
- Code wird für diesen bestimmten Prozessor compiliert

Was ist der Nachteil von virtuellen prozessoren?
- braucht eine Zwischenschicht(virtuelle maschine) zum echten Prozessor

Wofür brauche ich einen Debugger?
- Steuerung des Programms zur Laufzeit
- inspektion des Zustands zu jedem Zeitpunkt


## Programmierparadigmen

Wie unterteilen sich Programmiersprachen?
- systemorientierte Sprachen
- problemorientierte Sprachen

Wie unterteilen sich systemorientierte Sprachen?
- Maschienensprache
- Assembler

Wie unterteilen sich problemorientierte Sprachen?
- imperative Sprachen
- declarativer Sprachen

Wie unterteilen sich imperative Sprachen?
- strukturierte Sprachen
- prozedale Sprachen
- objektorientierte Sprachen

Wie unterteilen sich deklarativer Sprachen?
- logische Sprachen
- funktionale Sprachen

Welche Elemente hate eine strukturierte Sprachen?
- Seqenz
- Wiederholung
- Auswahl

### Objektorientierte Programiersprachen

Welche Konzepte von objektorientierter Sprache gibt es?
- strukturierte Daten und Funktionen
- Sprachkonzepte
	- vererbung
	- kapselung
	- polymorphie (mehr förmig)
- in der Regel prozedural
- Grundlage für kompenetenbasierte Entwicklung


### Funktionale Programiersprachen
- bestehen aus Funktionen im mathematischen Sinne
- sind durch Rekursion enebnso mächtig wie imperative oder objektorientierte Sprachen
- Funktionen haben keine Seiteneffekte
- lassen sich gut parallelisieren
- bestimmte Probleme lassen sich mit wenig Code lösen
- ungeeignet für andere Sachen


### dynamische Programiersprachen
- keine scharfe Abgrenzung
- führen Tätigkeiten zur Laufzeit aus
- dynamisch typisiert
- typische Eigenschaften
	- automatische speicherverwaltung
	- eval (meta programmierung)
	- objektsysteme zur Laufzeit veränderbar
	- duck typing (keine scharfe typüberprüfung)
	- reflexion (fähigkeit informationen über sich selbst zu bekommen)

## Algorithmen
- kurz
- präzise
- eindeutig

Was ist ein Algorithmus?
- eine endliche Menge von konkreten Anweisungen, die ein bestimmtes Problem lösen.

Was ist eine Datenstuktur?
- Eine Datenstruktur ist ein Modell, das die zur Lösung eines Problems benötigten Informationen (Ausgangsdaten, Zwischenergebnisse, Endergebnisse) enthält und für alle Informationen genau festgelegte Zugriffswege bereitstellt.

Welche Teile gehören zu einer Datenstruktur?
- Ausgangsdaten, Zwischenergebnisse, Endergebnisse

Benötigt ein Algorithmus eine bestimmte Datenstruktur?
- die beste organisation von daten gibt es nicht

Was ist ein Programm?
- besteht aus datenstrukturen
- besteht aus algoritmen
- ist auf einem computer lauffährig

Was definiert einen Präprozessor?
- Unabhängig von der Sprache c
- Direktiven beginnen mit eine ```#``` am Anfang

Welche Aufgabe erfüllt der Präprozessor?
- Lexiakalische Ersetzung

Erläutern sie die Fuktionen des Präprozessors
- #include: Setzt den Inhalt der Datei ein
- #define a b: Ersetzt alle künftigen Vorkommen von a durch b
- #undefine a: Vergisst den define a wieder
- #ifdef a ... #endif: Lässt den Block unter eine Bedingung im Source Code

Welche Arten von Fehlern kann ein Compiler zurück liefern?
- Lexikalische Analyse (falsche Zeichen, nicht geschlossene ```"```, Fehlende ```;```)
- Syntaktische Analyse (Überprüft Klammern bei Funktionsaufrufen)
- Semantische Analyse (Überprüft die Sinnhaftigkeit, z.B. Anzahl & Art der Parameter oder Deklaration von Variablen und Funktionen)

Workflow:
1. Compiler übersetzt c Code in Maschinensprache (.c in .o) 
2. Linker verknüpft einzelne .o (Out) Files in ausführbares Programm

Welche Aufgabe übernimmt ein Linker?
- Montiert aus vorhandenen Object Files ein ausführbares Programm

Welche Variablennamen sind gültig?
- Buchstaben, Ziffer, Unterstriche
- Erstes Zeichen keine Ziffer

Übertragen sie Variablen in snakecase usw
- Snakecase: ```peter_zwegat``` (Historisch für c)
- Camelcase: ```peterZwegat``` (Modern ;))
- Kebapcase: ```peter-zwegat```
- Pascalcase: ```PeterZwegat```
- Uppercase: ```PETER_ZWEGAT``` (Verwendet man häufig für Präprozessor Variablen)

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