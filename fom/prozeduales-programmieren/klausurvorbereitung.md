---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-01-27T15:04:59.926Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:53:06.780Z
---

# Klausurvorbereitung

## Teil 2:

Was ist eine Programierrsprache?
- eine formale Sprache
- beschreiben Algorithmen die auf einer Maschine ausgeführt werden
- Schnittstelle zwischen Programmierer und Maschine 
---

Was ist Hardware?
- eine fest installierte physische Grundlage 


Was ist Software?
- bestimmt welche Aufgaben auf der Hardware ausgeführt werden

Was ist der Vorteil von der Aufspaltung von Hardware und Software?
- Abbildung verschiedener Funktionen mit Software ohne Hardwareänderung

---

Was zeichnet eine von Neumann-Architektur aus?
- eine Rechnerarchitektur die Zentaleinheit und Hauptspeicher trennt 
- der Hauptspeicher enthält Daten auf dem ein Programm operiert, und das Programm selbst
- den Flaschenhals da die ALU und die Steuerung der Zentraleinheit konkurierend auf den Speicher zugreifen
---

Was ist eine Turingmaschine?
- ein theoretisches Konstrukt
- für Lösung eines mathematischen Problems
- Reduziert in den Anforderungen
- kleinste Möglichkeit zur Berechnung
- kann jeden Algorithmus der in endlicher Zeit berechnet werden kann, berechnen
- wenn es ein Computer ausrechnen kann, kann es die Turingmaschine auch -> Turing Vollständigkeit

Wie schreibt Turingmaschine auf das Band?
- Je nach aktuellen Zustand und Zeichen welches gelesen wurde, bewegt sich die Turingmaschine in 
eine in der Übrgangsfunktion definierte Richtung, und schreibt den Buchstaben welcher in der Übergangsfunktion steht auf das Band.
---


Was bedeuted Speicherprogrammiert?
- umsetzung der Programmlogik erfolgt Hardware unabhängig

Woher holt sich der Prozessor seine Anweisungen?
- aus dem Speicher

Welche Sprache versteht ein Prozessor nativ?
- Maschinensprache 

#### Maschinensprache
Wofür ist das Anfällig?
- programmierfehler
- schwer zu debuggen

Wie wurde das vereinfacht?
- mit dem Assembler
- Assembler ist eine schönere Schreibweise für eine Maschinensprache.
- Assemblercodes sind von Prozessor zu Prozessor unterschiedlich.

Was sind die Schwierigkeiten mit dem Assembler?
- zeitaufwendig
- fehleranfällig
- maximale Maschienennähe => maximale Problemferne

Was macht eine Hochsprache?
- Abstrahiert Assembler in eine Sprache die Näher an der menschlichen Sprache ist

Was ist die Aufgabe eines Compilers?
- Quellcode in Maschinensprache zu übersetzen

Was ist der Unterschied zwischen Assembler und Compiler?
- Assembler wird lexikalisch in Maschinensprache übersetzt
- Compiler übersetzt eine Hochsprache in Maschinensprache

Wie ist ein Compiler aufgebaut?
3 Gliedrig

Front End
- analysiert Quellcode
- erzeugt eine semantisch äquvivalente Darstellung in Form eines Zwischencodes

Middle End
- kann mit den Front-End-Daten arbeiten und optimierungen vornehmen

Back End
- erzeugt die Maschinensprache
- abhängig von Zielhardware

Was muss bei einer neuen CPU passieren?
- neues Back End

Was benötigt man für eine neue Programmiersprache?
- neues Front End

Was passiert im Front End?
- lexikalische Analyse -> Zerlegen des Quellcodes in "Token" (= atomare Bestandteile)
- preprocessing -> automatisiertes Suchen und Ersetzen (vgl. Präprozessor) auf Tokenstrom
- syntaxanalyse -> Funktion übernimmt "Parser", der über eine "Grammatik" gesteuert wird und einen sog. "Parse Tree" (besseres Format zur weiteren Optimierung) erzeugt.
- semantische analyse -> Anreichern des Parse Tree, um semantische Informationen

Was passiert im Middle End?
- Inline expansion 
- Dead code elemination
- Constant folding
- Loop optimization
- automatische parallelisierung

Was passiert im Back End?
- Analyse (Datenflussanalyse, Abhängigkeitsanalyse, Pointeranalyse)
- erzeugen des Maschinencodes
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
- Maschinensprache
- Assembler

Wie unterteilen sich problemorientierte Sprachen?
- imperative Sprachen
- deklarative Sprachen

Wie unterteilen sich imperative Sprachen?
- strukturierte Sprachen
- prozedurale Sprachen
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


### Funktionale Programmiersprachen
- bestehen aus Funktionen im mathematischen Sinne
- sind durch Rekursion ebenso mächtig wie imperative oder objektorientierte Sprachen
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

Abkürzung | Ausgeschrieben
-|-
```x += y``` | ```x = x + y```
```x -= y``` | ```x = x - y```
```x *= y``` | ```x = x * y```
```x /= y``` | ```x = x / y```
```x %= y``` | ```x = x % y```
```x++```    | ```x = x + 1```
```x--```    | ```x = x - 1```
```++x```    | ```x = x + 1```
```--x```    | ```x = x - 1```

Was ist ein Casting?
- Typumwandlung einer Variable

Wofür benötige ich einen Casting?
- Um aus einem float (2.0) ein int (2) zu machen:

Beipsiel von Casting
```
float a = 2.0;
int b = (int) a; // b = 2
```

Platzhalter kennen

- %s (Zeichenkette („String“))
- %d (Ganze Zahl)
- %i (signed integer)
- %f (float)
- %lu (unsigned long)
- %ld (signed long)
- %u (unsigned char)

Erläutern sie den Unterschied zwischen while und for:
- While Schleife hat nur einen Testausdruck (Bedingung)
- For Schleife hat Initialisierungsstatement, Testausdruck, Updatestatement

Erläutern sie die Aufgabe von break:
- Bricht die Schleifenausführung ab

Was ist ein Stellenwertsystem?
- Jede Ziffer hat einen unterschiedlichen Wert abhängig ihrer Position in der Zahl
- Der Wert der Zahl berechnet sich aus der Summe aller Ziffern zur Basis

Warum hat int einen Werteberech?
- Ein int wird in entweder 2 oder 4 Byte gespeichert
- Aus den begrenzten Kombinationsmöglichkeiten der Bits im Speicherbereich, ergibt sich ein begrenzter Wertebereich

Warum hat signed int einen asymmetrischen Wertebereich?
- Keine -0 oder +0 sondern nur 0

Was ist ein Byte?
- 8 Bit
- 2 Nibble

Was ist ein Short-Curcuit/Kurzschlussoperator?
```ausdruck1 && ausdruck2```
Wenn ausdruck1 false ist, wird ausdruck2 nicht mehr evaluiert
```ausdruck1 || ausdruck2```
Wenn ausdruck1 true ist, wird ausdruck2 nicht mehr evaluiert

Exclusives Oder:
```!ausdruck1 != !ausdruck2```

Warum sollte man keine Gleitkommazahlen miteinander vergleichen?
- Rundungsfehler
- Um so länger die Zahl nach dem Komma, umso größer wird der Rundungsfehler

- durch Ungenauigkeiten in Rechnungen
- float Zahlen haben nur eine endliche Genauigkeit
- da nach jedem Rechenschritt in das float gekürzt wird und Rundungsfehler enstehen
- Lösung wäre eine Toleranz von Abweichungen

Wass passiert wenn ich kein Nullbyte habe?
- Geht das Array immer weiter durch
- Lande ich in einem Speicherbereich außerhalb des Arrays, killt mich der Prozessor

Was ist ein Stack?
- Ein Stack ist ein Stapelspeicher

Wie funktioniert ein Stack?
- LIFO (Last In First Out)
- Ich leg was drauf und des muss ich als nächstes wieder weg nehmen
<p><a href="https://commons.wikimedia.org/wiki/File:Data_stack.svg#/media/Datei:Data_stack.svg"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Data_stack.svg/1200px-Data_stack.svg.png" alt="Data stack.svg" style="width: 500px"></a></p>

Was haben Funktionen mit einem Stack zu tun?
- Callstack enthält Informationen über Methoden-Rücksprung



Was können sie machen wenn sie mehrere Werte einer funktion zurück gben möchten?
- Werte via Pointer (übergeben an aufgerufene Methode via Methoden-Parameter) an den Methoden-Aufrufer zurückgeben

Was ist der Untschied zwischen der Übergabe via Wert oder Referenz?
- Übergabe via Kopie: aufgerufene Methode erhällt Kopie des Variablenwertes. Kopie kann ohne Seiteneffekte verändert werden.
- Übergabe via Referenz: aufgerufene Methode erhält Verweis auf einen Speicherbereich (Pointer). Veränderung des Wertes in dem Speicherbereich durch die aufgerufene Methode wirkt sich auf die aufrufende Methode aus.

Was ist ein buffer overflow?
- Über- oder unterschreiten des zulässigen Wertebereichs einer Variable

Erkläre Signed/Unsigned:
- Signed: Mit +/-. Variablenwerte sind Positiv oder Negativ
- Unsigned Ohne +/-. Variablenwerte sind immer Positiv

Wie geht eine Funktion ohne Rückgabe?
- Funktion-Rückgabewert ```void``` 

Was versteht man unter Rekursion?
- Eine Funktion welche sich selbst aufruft

Was versteht man unter einem pointer?
- Ein Pointer ist ein Zeiger auf eine Speicheradresse.

Was versteht man unter einem Nullpointer?
- Ein Nullpointer ist ein Zeiger auf eine spezielle Speicheradresse 0. Dies ist eine nicht gültige Adresse. Er wird verwendet um die Absenz eines Wertes darzustellen.

Was ist Pointerarithmetik?
- Rechnen mit Speicheradressen.

Wofür verwendet man Pointer?
- Verweis auf Speicher-Adressen

Wann brauche ich malloc und free
- malloc: Für die variable Speicherreservierung zur Laufzeit eines Programmes
- free: Zur Freigabe von nicht mehr benötigten, zuvor reservierten Speicher (Vermeidung von memory leaks)

<b>Speicher muss immer freigegeben werden.</b>

ENUM sind nicht Klausurrelevant

## Übungsaufgaben die man können soll
- Erkennen von Hex werten
- Umgang mit Einheiten
- Nullbyte verschieben können
- chomp Funktion anwenden
- 2 Strings zusammen fügen
- Strings zerlegen
- String an einem bestimmten Zeichen zerlegen
- Umformung Array-Notation zu Pointer-Notation
- Benutzung von malloc und free

- Schaltjahr
- Übung 11