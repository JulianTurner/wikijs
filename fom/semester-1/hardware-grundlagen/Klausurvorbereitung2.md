---
title: Klausurvorbereitung 2
description: 
published: 1
date: 2022-02-11T15:42:00.943Z
tags: 
editor: markdown
dateCreated: 2022-02-03T15:11:53.417Z
---

# Prüfungsvorbereitung

## ISA

- 2. Ebene eines Computers (über Ebene 1 - Microarchitecture)
- Befehlssatzarchitektur-Ebene (ISA = Instruction Set Architecture)
- Beinhaltet Befehlssatz des Computers
- Handbuch für Befehlssatz wird vom Prozessor-Hersteller zur Verfügung gestellt

## Microarchitecture

- 1. Ebene eines Computers (über Ebene 0 - digitale Logik)
- Besteht aus
  - 8 bis 32 Register
  - ALU (Arithmetic Logic Unit - Rechenwerk)
- Register sind mit ALU verbunden um einen Datenpfad (Data Path) zu bilden.
- Data Path Aufgaben:
  - Auswahl von 1 oder 2 Register mit denen die ALU arbeitet
  - Ergebnis ALU Operation in Register ablegen

## System Design

Alle Elemente eines Computersystems außer der Zentraleinheit.

# Implementation eine Computers

### Logikimplementation

Definition abstrakter Logikblöcke

### Schaltungsdesign

Entwurf der Maschine auf Transistor-Ebene

### Physikalische Implementierung

Eigentliche Implementation

### Designvalidierung

Test einer Maschine als komplexes Gesamtsystem

## Von Neumann und Harvard Architektur

### Von Neumann Architektur

- Grundlage fast aller moderner Computer
- Besteht aus
  - Rechenwerk (ALU)
  - führt Rechenoperationen und boolsche Verknüpfungen aus
  - Steuerwerk
    - interpretiert Anweisungen eines Pgoramms
  - Bus-System
    - Verknüpft die anderen Komponenten
  - Speicherwerk
    - speichert Programme und Daten, welche für das Rechenwerk zugänglich sind
  - Eingabewerk/Ausgabewerk
    - steuert Ein- und Ausgabe von Daten zu Anwender (Tastatur, Bildschirm) und anderen Systemen (Schnittstellen)

### Harvard Architektur

- Programm und Daten liegen in getrennten Speichern
- Heute geteilter Speicher im Bereich CPU Cache verbreitet

## Stack

- Kellerspeicher
- Lineare Datenstruktur
- Wächst von unten nach oben
- Enthält Rücksprungadressen und lokale Variablen
- automatisches Aufräumen von Variablen beim Verlassen eines Scopes

## Heap

- dynamischer Speicher (engl. Heap = dt. Haufen)
- Hierarchiche Datenstruktur
- enthält globale Variablen
- manuelle allocation und deallocation durch Programmier-Befehle

## CPU Kontrolleinheit

### Fest verdrahtet

- Fest verbaute logische Gatter dienen zum erzeugen der Kontrollsignale
- Schneller als microprogrammierte Signalerzeugung
- RISC Architektur basiert auf fest verdrahteter Kontrollsignalerzeugung

### Mikroprogrammierung

- Kontrollsignale -> Operation Mapping gespeichert als Kontrollwörter in speziellem, nicht via normalem Programmieren erreichbaren Speicherbereich
- Kontrollsignale werden programmatisch generiert
- Langsamer als fest verdrahtete Kontrollsignalvermittlung, wg. Aufrufzeit der Microinstruktionen vom dedizierten Speicher.

<!-- #### vertikaler Microcode
- Steuersignale repräsentiert mit decodiertem Binärformat
- Erlaubt hohen Grad an parallelisierung
- Benötigt keine zusätzliche Hardware
- Lange Kontrollwörter
- Jedes Bit in Kontrollfeld entspricht einer Kontrolllinie

#### Horizontaler Microcode
- Steuersignale repräsentiert mit encodiertem Binärformat
- Niedriger Grad an parallelisierung (gerade soviel wie Decoder zulässt)
- Benötigt zusätzliche Decoder Hardware, welche enocodiertes Binärformat in decodierte Steuersignale übersetzt -->

## CISC

**complex instruction set computer** zeichnen sich durch komplexte Befehlssätze aus
x86 Architektur (außen)

Vorteile:

- kann effizent programmiert werden (kompakter Code & wenig Speicher)
- elegant zu programmieren
Nachteile
- komplexe Maschine
- langsame Programmausführung da Pipelining schwierig (unterschiedliche Instruktionslänge)
- komplexe Instruktionen werden oft nicht genutzt

## RISC

**reduced instruction set computer** zeichenen sich durch simple Befehlssätze aus
M1 Prozessor

- wenige unterschiedliche Instruktionen
- Load-Store-Architektur (Operanden müssen erst in Registern geladen werden)
- Steuerung ist meist fest verdrahtet
- Befehle haben im Idealfall die gleiche Länge um Pipelining zu ermöglichen

## VLIW

**very long instruction word** bietet nach außen ein Programmierinterface an

- vergleichbar mit horizontalem Mikrocode

## Parallelrechner

Bestehen aus einer Vielzahl von traditionellen Prozessoren
Hauptbegriffe:

- symetisches (gleiche Prozessoren werden zusammengefasst zu einem) vs asymetrisches Multiprozessing (Master & Slave Prozessor)
- shared Memory (UMA = gemeiner Speicher, gleiche Datenzugriffszeiten) vs "NUMA" (jeder Prozessor hat seinen eigen schnellen Speicher, wenn auf anderen Speicher zugegriffen wird, dann wird die Zugriffszeit länger)
- Verbindungstopologie (Bus, Stern, Hyperkubus)

# Rechnerarchitektur

## SISD - klassischer 1-Kern-Prozessor

- Single Instruction, Single Data
<img src="https://upload.wikimedia.org/wikipedia/commons/a/ae/SISD.svg" style="background:#FFF">

## SIMD - Vektorrechner + Mehrkern-Prozessor

- Single Instruction, Multiple Data
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/21/SIMD.svg/400px-SIMD.svg.png" style="background:#FFF">

## MIMD - Grafikkarten

- Multiple Instruction, Multiple Data
<img src="https://daridesignstudio.com/wp-content/uploads/2021/03/Komputer-MIMD.png" style="background:#FFF">

## Benchmark

Schwierig Ergbnisse zu vergleichen, aufgrund von fehlender Aussagekraft.
Ergbis vom Benchmark weicht vom Realen Einsatzzweck häufig ab.
Am besten kann man Rechner unter real Bedingungen vergleichen.

## Einheiten

### MIPS

"Million Instructions Per Seconds"
Kann mit NOP(NO OPERATION) in die Höhe getrieben werden.

### FLOPS

"Floating Point Operations Per Second"
Hier wird mit Fließkommazahlen gerechnet.
Kein NOP möglich, es muss tatächlich gerechnet werden.

# Hardwaregrundlagen

## Reine Mechanik

Staffelräder, Sprosenwalzen, Schaltgliedtechnik, Zahnräder
Nachteil:

- anspruchsvoll in Produktion da mechanisch präzise

## Relais

elektromechanische Schaltungen
Nachteil:

- immernoch viel Mechanik

## Röhren

Nachteil:

- hohe Verlustleistung durch nötige Heizung
- hohe mechanische Empfindlichkeit
- hoher Platzverbedarf

## Transistorn

Vorteil:

- benötigt keine Heizung
- uneingeschränkte Lebensdauer
- relativ kompakte Form
- kürzere Schaltzeiten

## Integrierte Schaltungen

mehrere Bauelemente werden auf einem Plättchen zusammengefasst und durch
aufgedampfte Metallisierungslagen miteinander verbunden
Vorteil:

- geringe Größe
- geringer Stromverbrauch
- hohe Schahltgeschwindigkeit

## Speichersysteme

### Hauptspeicher (Arbeitsspeicher)

Heutige Hauptspeicher beruhen auf integrierten Schaltungen und können in statischen & dynamischen Speicher unterteilt werden.

#### Statischer Speicher

- jede Speicherzelle behält ihren Wert bis zur nächsten Änderung (Flip-Flop)
- verliert den Wert beim lesen nicht
- Nachteil: technisch Aufwendig

#### Dynamischer Speicher

- Schaltungstechnik ist deutlich einfacher
- Benötigt "Refrsh-Zyklen" um den Wert nicht zu verlieren

## Ein-/Ausgabegeräte

### Block Device

Schreiben und lesen in einem ganzen Datenblock
z.B. Magnetplatten & Bänder

### Char Device

Schreiben und lesen in einem Einzelzeichen
z.B. Terminal, Maus, Tastatur

## Festplatte

Magnetischer Datenträger mit drehenden Platten, mit einem mechanischen Arm der einen Schreib- und Lesekopf trägt.

Nachteile:

- Seek-Zeit ist hoch
- Rotational Latency ist hoch
- Anfällig gegenüber mechanischer Einwirkung

## SSD

Datenträger auf der Basis von nicht flüchtigem Flash-Speicher deren Kern aus modifiziertem MOSFETs gebildet wird.
Qualität der SSD ist u. a. abhängig vom Speichercontroller.
Speicherzelle nutzt sich mit Schreib- und Löschzyklen ab.

Vorteile:

- keine mechanischeschen Bauteile
- keine Seek-Zeit
- keine Rotational Latency
- keine Anfälligkeit gegenüber mechanischer Einwirkung

## NAND und NOR Flash

Bei NOR-Flash sind die Speicherzellen parallel verschaltet.
Der Zugriff auf die Speicherzellen erfolgt wahlfrei und direkt

- kurze Zugriffszeiten
- nicht flüchtiger Speicher auf Motherboard (BIOS)

Bei NAND-Flash ist wegen der internen seriellen Verschaltung das Lesen und Schreiben nur in Blöcken möglich.
Da Daten auf Festplatten ebenfalls Blockweise gelesen und geschrieben werden, eignet sich NAND-Flash als Massenspeicher, wie Speicherkarten, USB-Sticks und SSDs.

- platzsparend da weniger Datenleitungen
- höhere Speicherdichte
- geringere Kosten
- schnellere Schreibgeschwindigkeit
- geringer Stromverbrauch

## RAID

RAID (Redundant array of independent disks) kann mit Software oder Hardware-Controller realisiert werden.

Vorteile (ggf. - abhängig von RAID Typ)

- Ausfallsicherheit
- höhere Schreib-/ Lese-Raten

Nachteile (ggf. - abhängig von RAID Typ)

- Speicherplatz für Ausfallsicherheit kann nicht für Nutzdaten verwendet werden
- Schreiben evtl. langsamer als mit nur 1 Laufwerk, wenn Parität berechnet werden muss
- Ohne Parität (RAID 0) gefährdet der Ausfall einer Platte die Nutzbarkeit der Daten auf allen anderen Platten

<details>
  <summary>RAID Typen</summary>
  <table><thead><tr><th>RAID Typ</th><th>Min Laufwerke</th><th>Verteilung</th><th>Parität</th><th>Durchsatzrate</th><th>Platz verloren für Sicherheitsgewinn</th></tr></thead><tbody><tr><td>RAID 0</td><td>2</td><td>Blöcke-</td><td>Keine</td><td>Hoch</td><td>Keine</td></tr><tr><td>RAID 1</td><td>2</td><td>Keine</td><td>Spiegelung</td><td>2x Lesereate, 1x Schreibrate</td><td>Alle bis auf 1 Platte</td></tr><tr><td>RAID 3</td><td>3</td><td>Bytes</td><td>Striping – 1 Parität auf dedizierter Platte</td><td>Lesen hoch, Schreiben etwas langsam</td><td>effektiv 1 Platte</td></tr><tr><td>RAID 4</td><td>3</td><td>Blöcke</td><td>Striping – 1 Parität auf dedizierter Platte</td><td>Lesen hoch, Schreiben etwas langsam</td><td>effektiv 1 Platte</td></tr><tr><td>RAID 5</td><td>3</td><td>Blöcke</td><td>Striping – 1 Parität auf wechselnden Platten</td><td>Lesen hoch, Schreiben etwas langsam</td><td>effektiv 1 Platte</td></tr><tr><td>RAID 6</td><td>4</td><td>Blöcke</td><td>Striping – 2 Parität auf wechselnden Platten</td><td>Lesen hoch, Schreiben etwas langsam</td><td>Effektiv 2 Platten</td></tr></tbody></table>
</details>

Gut zu wissen:
Beim Bestücken eines RAID Laufwerk Arrays nicht Laufwerke aus der gleichen Charge verwenden (Höhere Chance das mehrere Laufwerke nach ähnlicher Nutzdauer gleichzeitig ausfallen).

## Drucker

## Was ist Information und Wissen

![wissenspyramide.png](/fom/semester-1/hardware-grundlagen/wissenspyramide.png)

## Umrechnen von Binär in Dezimal und umgekehrt ( evtl. Hexadezimal)

## Virtuelle Maschinen - Vor und Nachteile

Vorteil:
Hardware virtualisieren die nicht mehr existiert
Ich mehere Systeme auf einem Rechner laufen lassen
effizientere Auslastung der Hardware
Lizenskosten können gespart werden

Nachteil:
Single Point of failure
Overhead
Lizenskosten können anfallen

## Hardwarevirtualisierung

Typ 1 = Bare Metal Hypervisor
verfügt über alle Hardware Ressourcen
Typ 2 = hosted Hypervisor
verfügt nur über Host Ressourcen

## Bufferoverflow & StackOverflow

Beim Bufferflow scheibt ein Programm außerhalb des für des Programm alloziert Speicher.
Beim Stackoverflow wächst der Stack außerhalb des allozierten Stackspeicherbereich.

## Activation Record

für jeden Funktionsaufruf wird ein "Activation Record" auf den Stack gelegt.
Enthält:

- Rücksprungadresse
- Übergabeparameter
- lokale Variablen der aufgerufenen Funktion

## Devicetreiber

- müssen mit Hardware & Betriebssystem kompatibel sein
- fassen geräteabhängige Routinen zusammen
- Ansteuerung einer beliebigen Anzahl von Geräten gleichen Typs verwendet werden

## Soft- und Hardwareinterrupt

Während Hardwareinterrupts das Resultat von externen Unterbrechnungsanforderungen sind, werden Softwareinterrupts mit Hilfe spezieller Instruktionen ausgelöst.

Softwareinterrupts haben eine niedrigere Priorität als Hardwareinterrupts.

Innerhalb von Soft & Hardwareinterrupts gibt es eigene Prioritätslevel(Cache Miss hat höere Priorität).

## System Call

System Call ist der Unterbrechungswunsch der Anwendungssoftware, die Bearbeitung im Bertiebssystem fortzuführen.
Das Betriebssystem hat höhere Rechte als die Anwendungssoftware(Kontrollierter Zugriff auf Hardware).

## Deadlock

Prozess A wartet auf Beendigung von Prozess B.
Prozess B wartet auf die Beendigung von Prozess A.

## Race Condition

Mehere Prozesse arbeiten in einer undefinierten Reihnfolge. Ergebnis hängt von der tatsächlichen Reihnfolge ab.
z.B:
$2 * 1 + 3 = 2 + 3 = 5$
oder
$2 * 1 + 3 = 2 * 4 = 8$
