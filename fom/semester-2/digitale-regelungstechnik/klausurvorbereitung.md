---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-01-13T19:25:58.309Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:44:54.647Z
---

# Klausurvorbereitung

## [Einleitung und Grundlagen](einleitung_grundlagen.md)
Blockschaltbilder sollte man Zeichnen können (geschlossener Regelkreis, 2-Freiheitsgraderegelung)  
### Was ist eine Führungsgröße?  
Die eingegebener Zielwert z.B. Fluhöhe Quadrocopter 30m  

### Was ist eine Stellgröße?
Der Wert für die Aktoren z.B. Strom zum erreichen einer Drehzahl (5000 U/min beim Rotor)

### Was ist eine Regelabweichung?
Die Abweichung zwischen den Soll(Führungsgröße 50m) und gemssener Istwert (30m)  

### Was ist ein betrachtete System?  
Black Box Betrachtung
- nur das äußere Verhalten wird betrachtet
- Input & Output abhangig von Raum & Zeit
	- Materie, Energie, Informationen 
- Produktionsprozess zwischen Input & Output:
	- Stoffumwandlung, Energieumwandlung, Informationsumwandlung

![Blackbox](https://upload.wikimedia.org/wikipedia/commons/4/44/Blackbox3D.png)

### Was ist eine Regelung?  
![Regelung](regelung.png)


Beispiel:  
Klimaautomatik

Führungsgröße w(t): Einstellung Temperatur (20°C)  
Regelabweichung e(t): Abweichung zwischen Sollwert und Istwert (4°C)  
Stellegröße u(t): Strom für Gebläse    
Störgröße z(t): offnes Fenster    
Ausgangsgröße y(t): Lufttemperatur (Istwert 17°C)  
Messrauschen n(t): Position des Sensors  
Ist-Verlauf y'(t): Lufttemperatur (gemessen 16°C)

### Was ist der Vorteil und Nachteil einer Regelung?  
> Vorteil: Istwert wird mit dem Sollwert verglichen  
> Nachteil: technisch aufwendiger, keine direkte Kontrolle  

### Was ist eine Zwei-Freiheitsgrade-Regelung?  
![Zwei Freiheitsgrade Regelung](2-freiheitsgrade-regelung.png)
> Entweder ist die Steuerung oder die Regelung aktiv  
> Vorteil: Kombination aus Steuerung und Regelung  
> Nachteil: technisch aufwendiger  

Beispiel:
Tempomat  
Führungsgröße w(t): Einstellung Geschwindikgeit (120 km/h)  
Stellegröße u(t): mittlere Beschleunigung  
Störgröße z(t): Steigung     
Ausgangsgröße y(t): Geschwindigkeit (Istwert 100 km/h)

Bei Regelung:  
Regelabweichung e(t): Abweichung zwischen Sollwert und Istwert (20 km/h)

### Was ist der Unterschied zwischen einer Zwei-Freiheitsgrade-Regelung und Regelung?  
Die Regelabweichung wird deutlich schneller abgebaut.



## [Elementare Übertragungsglieder & Grundlagen Messtechnik](uebertragungsglieder.md)
### Nennen Sie 3 elementare Übertragungsglieder.  
P-Glied (proportional), I-Glied (integral), D-Glied (differential)  

### Was ist ein vollständiges Messergebnis?  
Messergebnis $\pm$ Messabweichung  

### Wonach unterscheidet man Messgeräte Kategorien?
Präzisionsmessgeräte, Feinmessgeräte, Betriebsmessgeräte

### Unterschied Präzession und Validität?
Präzision: Reproduzierbarkeit der Messergebnisse  
Validität: Güte der Messergebnisse  

### Erklären Sie warum der Unterschied zwischen präzise / nicht valide und präzise / valide interessant ist.
- Bei Wiederholung der Messung kann Unterschied nicht erkannt werden  

### Wie ermittelt man eine Messabweichung?
Abschätzung der Abweichung aus:
- Datenblatt des Herstellers
- Daten von der Kalibrierung
- Daten aus früheren Messungen

### Woraus setzt sich die Messabweichung zusammen bei indirekter Messung?
abhängig vom Einfluss auf einzelne Messparameter des Gesamtergebnisses

### Was ist der Unterschied zwischen Messgröße und Messwert?
Messgröße: physikalische Größe der Messung (Masse, Länge, Temperatur, Zeit)
Messwert: mit Abweichung behaftetes Abbild der Messgröße

### Welche Probleme gibt es bei der Abtastung beim Oszilloskop?
Balance zwischen zu ausreichenden Daten (keine Unterabtastung) und nicht zu vielen Daten (Datenvolumen)




## [Untersuchung der Systemdynamik](systemdynamik.md)
Verlauf analoges Signal geben => Umwandlung in Wert / Zeitdiskretes Signal  
Funktionsweise einen Theroelemts  
Wie funktioniert ein Thermoelemt  
Wie wird der thermoelektrische Effekt genutzt um eine Temperatur zu messen?  
Digitales unterabtasten von analogen Signalen  
Unterschied PTC/NTC    
PTC Regulierender Effekt  
Unterschied Widerstandsthermometer zu Thermoelement?  
Inkrementelle Messung braucht 2 lineare und braucht einen Endanschlag  
Bei einer absoluten Messverfahren braucht man keine Referenzfahrt, ist aber komplizierter  
Wie funktioniert ein potentiometrischer Sensor?  
Wie funktioniert ein Potentiometer?  
Wie funktioniert ein induktiv Sensor?  
Welche Möglichkeiten hat man bei einem Plattenkondensator die Kapazitätsänderung zu kontrollieren?  
Plattenkondensator => Änderungsparameter  




## [Regelkreise und Übertragungsglieder](regelkreise.md)
Wirkungsplan
![](wirkungsplan.png)
### Wofür ist ein Aktor zuständig?
Umsetzung des elektrischen Regelsignals in eine physikalische Stellgröße
Der Aktor ist das einzige Element welches tatsächlich in das Regelsystem eingreift. 

### Sensoren und Aktoren sind beides Wandler. Was unterscheidet sie?
Der Sensor erfasst eine nichtelektrische physikalische Größe.
Der Aktor erzeugt eine nichtelektrische physikalische Größe.

### Erklären Sie die Wirkungsweise eines piezoelektrischen Bauteils
Mechanische deformation erzeugt eine proportionale elektrische Spannung.
Anlegen einer elektrischen Spannung erzeugt eine mechanische Deformation.

### Mikroelektronik Vor- und Nachteile  
Vorteile:
- hohe Dynamik
- genaue Positionierung
- geringe Geräuschbelastung für Menschen
- keine elektromagnetisches Feld im Außenbereich
Nachteile:
- größere Geräuschbelastung für manche Tiere
- Kräfte gering (mit anderen Systemen lösbar)

### Beispiele für Einsatz von Piezoelementen
- Piezoinjektion
- Klopfsensor
- Piezofeuerzeug
- Druckkopf vom Tintenstrahldrucker
- 3d Drucker
- **D**igitel **L**ight **P**rocessing Beamer


### Nennen Sie Beispiele für fluid mechanische Aktoren  
Pneumatikzylinder, Hydraulikzylinder, Pneumatischer Muskel

### Vor- und Nachteile von fluid mechanischen Aktoren
Vorteile:
- hohe Kräfte möglich
- Orts- und Neigungsunabhängig
Nachteile:
- Verschleiß durch Bewegung

## [Regelstrecken](regelstrecken.md)
Regelstrecke mit Ausgleich
Was ist die Verzugszeit bei einem $PT_1 \space System$  

## [Regler](regler.md)
Ist es möglich mit einem P-Glied eine stationäre Genauigkeit zu erreichen?  
Zeichnen Sie einen Regelkreis und beschriften sie?  
Unterschied zwischen P PI und PID Regler  
Graphen beschriften  


