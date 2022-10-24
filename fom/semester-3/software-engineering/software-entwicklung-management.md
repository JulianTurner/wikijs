---
title: Software- Entwicklung & -Management
description: 
published: 1
date: 2022-10-24T14:39:10.677Z
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