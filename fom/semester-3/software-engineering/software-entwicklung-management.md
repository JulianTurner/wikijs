---
title: Software- Entwicklung & -Management
description: 
published: 1
date: 2022-10-24T16:42:56.064Z
tags: 
editor: markdown
dateCreated: 2022-10-12T16:10:21.145Z
---

# Software-Entwicklung & -Management

## Software-Entwicklung und Basistechniken

Software Entwicklung verwendet Prinzipien, Methoden und Werkzeuge für die ingenieurmäßige Entwicklung und Anwendung von umfangreichen Softwaresystemen.

### Allgemeingültige Prinzipien

- nicht mit Kopf durch Wand rennen
- nicht Ast absägen, auf dem man sitzt

### Entwurfsprinzipien des Software Engineering

<!--- Eifügen Bild Script 3 Seite 20 - Abhängigkeit der Prinzipien --->

#### Prinzip der Abstraktion

Verallgemeinerung mit 3 Ebenen:
- Exemplar-Ebene: tatsächliche Handlungen, spezifische Ereignisse, konkrete Sachverhalte in ihren Beziehungen/zeitlichen Abläufen
- Typ-Ebene
	- generalisiert Aussagen mit Klassifizierung
	- passive Elemente (z. B. Kunde, Mitarbeiter, Konto)
	- aktive Elemente: Handlungen/Aktivitäten bzw. Ereignisse an denen passive Elemente beteiligt sind (z. B. Konto eröffnen)
- Meta-Ebene
	- strukturierte passive Elemente -> Klassen
	- unstrukturierte passive Elemente -> Attribute von Klassen
	- aktive Elemente -> Operationen von Klassen

#### Prinzip der Strukturierung

- Sichtbarmachen großer Zusammenhänge unter Weglassung bestimmter Details
- Darstellung bestimmter Details ohne alle Details darzustellen
- Herstellung eines bestimmten Zusammenhangs (nicht zwangsläufig hierarchisch)
- Unterscheidung von statischen, dynamischen und organisatorischen Strukturen

#### Prinzip der Hierarchisierung

Strukturierung mit erzwungener Rangfolge

#### Prinzip der Modularisierung

- Große Lösung gegliedert in kleineren, überschaubaren Teillösungen
- Jedes Modul = benannte, in sich geschlossene, abgegrenzte Einheit/Komponente eines Systems
- Verwendung eines Moduls erfordert keine Kenntnisse über inneren Aufbau des Moduls
- Außen-Kommunikation mit Modul via klar definierter Schnittstellen
- Interne Moduländerungen haben keine Seiteneffekte
- jedes Modul einzeln testbar ohne Einbettung ins Gesamtsystem

#### Bindung und Kopplung

- Kohäsion: Maß für Stärke des inneren Zusammenhangs eines Moduls
	- höhere Kohäsion wünschenswert (High Cohesion)
- Kopplung: Maß für die Abhängigkeit zwischen zwei Modulen
	- geringe wechselseitige Kopplung zwischen Modulen wünschenswert (Low Coupling)
  
  
#### Geheimnisprinzip (Information Hiding)

- Jede Komponente erbringt vollständige Leistung
- Außerhalb nur bekannt was die Komponente macht
- Wie die Leistung erbracht wird ist außen nicht sichtbar
- Angewendet um Entwurfsentscheidungen vor Anwendern zu verbergen => ermöglicht leichtes Ändern der Entwürfe ohne Anwender darüber zu informieren

#### Prinzip der Lokalität

- Alle benötigten Informationen für Lösung eines Problems an einem Ort (auf einer Seite)
- Nicht benötigte Infos ausblenden/auslagern

Unterstützt durch:
- Entscheidungstabellen
- Hierarchische Zustandsautomaten
- Objektorientierte Analyse (OOA)

Erschwert durch:
- Vererbung (Infos müssen entlang Vererbungsbeziehungen zusammengesucht werden)
- Programmiersprachen die keine Methoden-Verschachtelung erlauben (Bsp.: C++, Java)

#### Prinzip der Verbalisierung

Begriffe, Klassifizierungen u. Namen müssen sich an Namensgebung Vorschrift/Regeln orientieren.

Erreicht durch:
- aussagekräftige Namensgebung ("sprechende" (Variablen-)Namen)
- geeignete Kommentare
- selbst dokumentierende Konzepte und Sprachen

#### Abhängigkeit der Prinzipien

<!-- TODO 03a Seite 20 Abhängigkeit-Grafik einfügen -->

#### Prinzip der Wiederverwendbarkeit

- Können Lösungen vollständig/Teile von Lösungen beschafft werden?
- Können Komponenten aus Bibliothek genutzt werden?
- Können Architektur- oder Entwurfsideen wiederverwendet werden?
- Kann geplante Lösung angepasst werden um existierende Komponenten zu verwenden (evtl. abwägen, ob eine kleine Einbuße an Funktionalität für einen großen Gewinn bei Entwicklungszeit/-kosten möglich ist)

#### Prinzip der Ästhetik

- Wahl und konsequente Verwendung eines Architekturstils
- Architektur Struktur für Struktur des Problems angemessen
- Wahl der einfachsten und klarsten Lösung aller möglichen Lösungen

#### Qualitätsprinzip

Ein guter Entwurf ist

- effektiv: erfüllt Vorgaben und Löst Problem
- wirtschaftlich: gebrauchstauglich, kostengünstig und mehrfach verwendbar/verwendet
- softwaretechnisch gut: leicht verständlich, robust, zuverlässig, änderungsfreundlich

### Modell

Modell ist Ergebnis eines Abbildungsprozesses oder Systems mit Ziel, dessen Verhalten zu simulieren/analysieren.

### Softwareentwicklungswerkzeuge

- soll Effektivität (Ergebnis/Ziel orientiert) erhöhen
- soll Effizienz (Ergebnis/Ziel mit möglichst geringem Mitteleinsatz erreichen) erhöhen
- werden von talentierten Mitarbeitern für die Softwareentwicklung benötigt (sind <u>nicht</u> optional)
- ersetzen nicht Talent von Mitarbeitern - Mitarbeiter müssen für Aufgaben geeignet sein

Beispiel Funktionalität: Farbliche Codierung bei Syntax-Highlighting

Beispiel-Tools:
- Geschäftsprozessmodellierung: ARIS-Toolset
- Integrierte Entwicklungsumgebung (IDE): Eclipse, IntelliJ IDEA, ...
- Versionierung: CVS, Subversion, Git
- Testen: JUnit
- Fehler-/Änderungsmanagement: Bugzila

### ARIS Konzept

Architektur integrierter Informationssysteme

Fünf Sichten-Architektur:
- Organisationssicht (Modelltyp: Organigramm)
- Datensicht (Modelltyp: Entity-Relationship-Model (ERM))
- Steuerungssicht (Modelltyp: Ereignisgesteuerte Prozesskette (EPK))
- Funktionssicht (Modelltyp: Funktionshierarchiebaum)
- Leistungssicht

Jede Sicht hat 3 Beschreibungsebenen:
- Fachkonzept
- Datenverarbeitung-Konzept
- Implementierungsebene (=> Architekturentwurf)

<!-- TODO 03a Seite 32 ARIS-Konzept Grafik einfügen -->

### Unified Modeling Language (UML)

Für Klausur relevant:
- Klassendiagramm
- Objektdiagramm
- Anwendungsfalldiagramm
- Aktivitätsdiagramm
- Zustandsdiagramm

## Qualitätsmodelle und -management

Grundproblem: Software ist immateriell => Qualität schwer messbar

### Relative Fehlerkosten über die Projektzeit

Kosten größer je später Fehler im Projekt aufgedeckt werden
Daher: mit Methoden Qualität frühzeitig prüfen/kontrollieren/sichern

### Qualität

- Fehlerfreiheit nicht einziger Qualitätsaspekt
- Fehlen von Qualität -> Nutzen der Software führt zu: Stress, Unzufriedenheit, Unbrauchbarkeit, Unnötigkeit, Lästigkeit
- Präsenz von Qualität -> Nutzen der Software führt zu: Zufriedenheit, Erstaunen

> Qualität ist der Grad in dem ein Satz inhärenter Merkmale Anforderungen erfüllt.

Software hat Qualität wenn sie
- korrekt ist (geforderte Funktionalität bietet)
- alle geforderten Eigenschaften besitzt

Software Engineering befasst sich mit:
- Projektqualität (Qualität des Projekts in dem Produkt hergestellt wird)
- Produktqualität (Qualität des Produkts)
	- Gebrauchsqualität (Qualität aus Sicht des Nutzers; Qualität die Kunde direkt fordert)
	- Wartungsqualität (Qualität aus Sicht eines Wartenden, Bsp.: Entwickler/Betreiber)
  
<!-- TODO: 03a Seite 44 Bedeutung QUalitätsaspekte über Zeit Grafik einfügen -->

#### Qualitätsmodelle und Qualitätsmanagement

- Qualität nicht automatisch in Software
- Qualität muss in Produkt hinein entwickelt werden
- Qualität-Stärke Abhängig von Qualitätsmodell
	- Starke Abhängigkeit zw. Prozess- und Qualitätsmodellen
		- Qualität muss durch Entwicklungsprozess sichergestellt werden (Bsp.: Think Aloud/Pair-Programming)
- Nicht jedes Projekt hat gleiche Qualitätsanforderungen (vgl. Steuerung Atomkraftwerk/Raumfahrt mit Internet-Infoseite)
- Qualitätsmanagement hat Aufgabe, aufgestellte Qualitätsanforderungen zu erreichen
	- Konstruktive Maßnahmen: Maßnahmen die aktiv während der Entwicklung beachtet werden müssen (Methoden, Sprachen, Richtlinien, Standards, ...)
	- Analytische Maßnahmen: Maßnahmen die diagnostisch existierendes Qualitätsniveau messen (Reviews, Inspektion, Testende Verfahren, ...)

#### Atomare Merkmale Prozessqualität

Merkmal | Anmerkung
---|---
Entwicklungseffizienz|hoch, wenn Entwicklungsaufwand gering
Entwicklungsgeschwindigkeit|hoch, wenn Resultat nach kurzer Zeit verfügbar
Termineinhaltung|hoch, wenn prognostizierte Termine genau eingehalten
Bausteingewinn|hoch, wenn viele verwendbare Software-Komponenten entstehen oder verbessert werden
Know-how-Gewinn|hoch, wenn Mitarbeiter neue Kenntnisse/Erfahrungen zu Anwendungen/Methoden/Werkzeugen erwerben
Projektklima|gut, wenn Mitarbeiter Zusammenarbeit als angenehm empfinden und wieder zusammenarbeiten würden

#### Kriterien erfolgreicher Qualitätsmessung

Kriterium | Anmerkung
---|---
Relevanz|Sind Beurteilungskriterien Kaufentscheidungskriterien für Kunden  => für Marketingentscheidungen relevant?
Vollständigkeit|Ermöglicht Verfahren Messung aller aus Kundensicht relevanter Qualitätsdimensionen?
Aktualität|Ergebnisse des Verfahrens aktuell?
Eindeutigkeit|lassen Ergebnisse eindeutige Rückschlüsse auf Qualitätsbeurteilung zu?
Steuerbarkeit|Liefern Ergebnisse Anhaltspunkte für gezielte Qualitätsverbesserung?
Kosten|Rechtfertigen Ergebnisse den finanziellen/personellen Aufwand des Messverfahrens?

## Software-Management

### Management von Software-Projekten

Risiko: ein potentielles Problem
Problem: ein Risiko, das eingetreten ist

#### Projekt-Vorhaben
- eindeutiges Ziel
- begrenzter Umfang
- individuelle Anforderungen
- hohe Komplexität
- Erfüllung bedingt Organisation, die für Umsetzung der Tätigkeiten eine Projektmethode anwendet
	- Projektmethode: plant, steuert, führt durch und kontrolliert anfallende Arbeiten

#### Maß/Metrik
- bezieht sich auf Eigenschaften eines Software-Entscheidungsprozesses/-Produkts
- versucht Erfüllungsgrad der Eigenschaften in einem Zahlwert auszudrücken

#### Projektmanagement
Anwenden von Wissen, Fähigkeiten Werkzeugen und Methoden in Vorgängen für die Erfüllung von Projekt-Anforderungen

Methoden-Beispiele: DIN 69901, ISO 10006, V-Modell XT

### Risiken managen

Risikomanagement: systematische Vorgehensweise über Korrekturmaßnahmen nachzudenken, bevor Problem auftritt (solange Problem noch abstrakte Vorstellung ist).

Gegenteil:
Krisenmanagement: Lösung für ein Problem finden, nachdem es aufgetreten ist.

#### Aktivitäten Risikomanagement-Prozess

Risiko-Bewertung:
Aktivität|Anmerkung
---|---
1. Risikoidentifikation|Aufstellen Liste projektspezifischer/-gefährdender Risikoelemente
2. Risikoanalyse|Bestimmung Risikofaktor = Eintrittswahrscheinlichkeit * Schadenshöhe
3. Risikoprioritätsbildung|Ordnung Risiken nach Priorität für Identifikation wirklich relevanter Risiken

Risikobeherrschung:
Aktivität|Anmerkung
---|---
4. Planung des Risikofalls|Eventualitätspläne (Was ist zu tun, wenn...) aufstellen
5. Risikominderung|Was kann vor Eintreten des Risikos getan werden
6. Risikoüberwachung|Kontinuierliche Überprüfung ob Risiko eingetreten

### Erfolgreiche Projekte

Herausforderung: <strong style="color:green">geforderte Leistungen</strong> mit <strong style="color:blue">hoher Qualität</strong> <strong style="color:Crimson">innerhalb des Budgetrahmens</strong> <strong style="color:Coral">rechtzeitig fertig</strong> stellen.

<!-- TODO 03a Seite 57 Grafik Magiesches Dreieck und Teufelsquadrat einfügen-->

### Besonderheiten IT-Projekte

Benötigt mehr Management als bei Produktionsprozess-Projekten:
- Funktionierende Projektüberwachung und -steuerung
- offene Kommunikation im Projekt und zum Auftraggeber
- Mitarbeiter fürdern und entwickeln
- Expertenmeinung ernst nehmen
- Entwicklungsprozess messbar gestalten
- Projekt in kleinere Einheiten zerlegen

#### Produkt (Software) ist immateriell
Sieht es nicht, nicht anfassbar, aber es ist immer fast fertig

#### Software Entwicklung nicht-deterministisch
- Neue Erkenntnisse während Entwicklung haben Auswirkung auf bisherige Ergebnisse
- Teilprodukt ist immer nur bedingt fertig
- oft Hälfte der Arbeitskraft für Überarbeitung bereits erstellter Teilprodukte benötigt

#### Kein klares Verständnis von Entwicklungsprozess
- keine Lange Historie wie bei anderen Ingenieursdisziplinen
- Erster Schritt immer: individuell passendes Vorgehensmodell finden

#### Einmaligkeit
- Viele IT-System-Entwicklungen absolut einmalig
- Gewonnene Erfahrungen von begrenztem Wert (Bsp.: erfolgreiche SAP Einführung kein Indiz für zukünftige erfolgreiche SAP Einführungen)
- Risiko des Scheiterns nur minimierbar, nicht eliminierbar
- Projekt hat hohe Komplexität und daher auch hohes Risiko

#### Unteilbarkeit der Arbeit
- Lösung eines Software-Problems erfordert intensive Beschäftigung eines Entwicklers mit dem Problem
- Übertragung von Aufgaben teuer, da neuer Mitarbeiter Einarbeitungszeit benötigt
- Spezialisten für bestimmte Probleme sind äußerst schwer ersetzbar
- In Projektplänen wird häufig davon ausgegangen, dass Mitarbeiter austauschbar sind (Personalresource auf Arbeitsmarkt einkaufen)

> Kein Plug & Play für Projektmitarbeiter
{.is-info}