---
title: Klausurvorbereitung 3
description: 
published: 1
date: 2022-02-09T18:23:14.210Z
tags: 
editor: markdown
dateCreated: 2022-02-05T08:20:41.063Z
---

Nennen Sie Vor- und Nachteile der Verwendung spezieller IO-Operationen für den 
Zugriff auf die Steuer- und Datenregister von Peripheriegerätesteuereinheiten.

Warum ist Polling und Interrupt für IO nicht im Skript ? S. 418

Wie viele Einträge benötigt eine solche Pagetable bei 4 GB Hauptspeicher und einer Seitengröße von 512 Bytes? S. 458
Größe des Speichers / Größe der Seitengröße = Anzahl der Seiten = Anzahl der Einträge in dem Pagetable

Wichtig für die Klausur:
Verständinis
Zusammenhänge erkennen
Bleistift und Radiergummi mitnehmen

Grundelegende Definition
Was ist eine von Neumann Architektur
# Welche Schwieriegkeiten hat eine von Neumann Architektur
Gleichzeite Zugriff konkurierend auf den Speicher von der Steuer und Recheneinheit

# Unterschiede zu Harvard Architektur
Steuer und Recheneinheit haben ihren eigenen Speicher

Zeichnung erklären von Neumann Architektur

# Schreiben Sie ein Programm welche zwei zahlen in folgenden Registern addiert
add ERGEBNISREG, REG1, REG2

# Führen sie eine Shift Operation durch(Befehl wird dann gegeben)
slr REG # right teilt 2
sll REG # left multipliziert 2

# Was kann ich mit einem Raid erreichen?
- Ausfallsicherheit
- Performance 

# Wie funktioniert ein Bus System?
- mehere Geräte anschließen und miteinander vernbinden verbinden
- seriell mit einer Leitung
- paralell mit meheren Leitungen
- Master & Slave
- Multimaster


# Wie groß war eine Festplatte früher? 
- unter 1 Mb, ähnlich wie trommelspeicher

Grundlagen der Schaltungstechnik
- Grundlegende boolische Funktion 
- Wahrheitstabelle
# Zusammengesetzte schaltung Wahrheitstabelle 
- 3 Eingnänge A | B | C | A & B | oder C

Zeichnen sie einen Full Adder aus 2 Half Adder
<img src="https://circuitverse.org/uploads/project/image_preview/157672/preview_2020-09-10_16_56_39_UTC.jpeg">
![wahrheitstabelle_fulladder.png](/fom/wahrheitstabelle_fulladder.png)

Warum hat man Ringe gebaut?
- erhöhte Sicherheit
- Stabilität da ein Nutzerprogramm nicht direkt auf Hardware zugreifft
- kompatibilität durch standartisierte Schnittstelle

Warum gibt es priviligierte Befehle?
- interrupts auslösen
- um in tiefere Schichten (Kernel) zu kommen / schützen

Aus welchen Bestandteilen besteht float?
- Mantisse
- Basis
- Exponent

# Was ist der Unterschied zwischen analog und digital?
analog: hat einen kontinuierlichen Werteraum.
digital: können nur Werte dargestellt werden

# Was kann man mit heutigen Rechnern bearbeiten?
- Skalare und Vektoren

# Wie werden Daten repräsentiert in einem Rechner?
- aus bits (0 oder 1)

# Umwandlung dezimal zu binär
- horner Schema (Achtung von unten nach oben)
# Wie kann ich in einem Rechner eine negative Zahl darstellen?
mit einem Vorzeichen Bit
2-er Komplement

# Wie Berechne ich das 2er Komplement?
Komplement der Zahl (1001 => 0110) oder (0000 => 1111)
1 Addieren (0110 + 1 = 0111) oder (1111 + 1 = 0000)

# Substraction mit dem 2er Komplement?
erst das Komplement bilden und dann addieren


Sie haben einen rechner der 0 oder 1 Gen, und sollen eine Subtraction druchführen. Wie geht das?
