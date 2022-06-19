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
Nennen Sie 3 elementare Übertragungsglieder.
Was ist ein vollständiges Messergebnis?
Wonach unterscheidet man Messgeräte Kategorien?
Unterschied Präzesion und Validität?
Wie ermittelt man eine Messabweichung?
Woraus setzt sich die Messabweichung zusammen bei indirekter Messung?
Was ist der Unterschied zwischen Messgröße und Messwert?
Welche Probleme gibt es bei der Abtastung beim Ozsiloskop?





## [Untersuchung der Systemdynamik](systemdynamik.md)
Verlauf analaoges Signal geben => Umwandlung in Wert/Zeitdiskretes Signal  
Funktionsweise einen Theroelemts  
Wie funktioniert ein Thermoelemt  
Wie wird der thermoelektrische Effekt genutzt um eine Temperatur zu messen?
Digitales unterabtasten von analogen Signalen
Unterchied PTC/NTC  
PTC Regulierender Effekt  
Unterschied Wiederstandsthermometer zu Thermoelement?
Inkrementelle Messung braucht 2 lineare und braucht einen Endanschlag  
Bei einer absoluten Messverfahren braucht man keine Referentzfahrt, ist aber komplizierter  
Wie funktioniert ein potentiometrischer Sensor?
Wie funktioniert ein Potentiometer?  
Wie funktioniert ein induktiv Sensor?  
Welche Möglichkeiten hat man bei einem Plattenkondensator die Kapazitätsänderung zu kontrollieren?
Plattenkondensator => Änderungsparameter  




## [Regelkreise und Übertragungsglieder](regelkreise.md)
Wirkungspläne  
Piezo Elemente  
Mikroelektronik Vor und Nachteile
Was ist die Verzugzeit bei einem $PT_1 \space System$ 
Nennen Sie Beispiele für fluidmechanische Aktoren 

## [Regelstrecken](regelstrecken.md)
Regelstrecke mit Ausgleich
## [Regler](regler.md)
Ist es möglich mit einem P-Glied eine stationäre Genauigkeit zu erreichen?  
Zeichenen Sie einen Regelkreis und beschriften sie?  
Unterschied zwischen P PI und PID Regler  
Graphen beschriften  