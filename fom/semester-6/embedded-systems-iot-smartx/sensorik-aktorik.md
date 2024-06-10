---
title: Sensorik & Aktorik
published: 1
date: 2024-03-04T19:35:10.207Z
tags: 
editor: markdown
dateCreated: 2024-03-04T19:35:10.207Z
---

# Sensorik & Aktorik

## Analoge Sensoren

- Passives Sensoren
  - benötigen eine Energiequelle
  - Messung von einem Spannungsabfall
  - Beispiele:
    - Heißleiter
    - Kaltleiter
    - [DMS](/fom/semester-5/mechatronik/sensoren.md#dehnungsmessstreifen)

- Aktive Sensoren
  - erzeugen ein elektrisches Signal
  - Messen von einer Spannung
  - Beispiele:
    - Thermoelemente
    - Photoelemente
    - Drucksensoren

- Analoge Sensoren
  - Messung von zeitkontinuierlichen Größen

- Digitale Sensoren
  - Messung von zeitdiskreten Größen
  - kann analoger Sensor mit A/D-Wandler sein (erzeugen PWM-Signal als Ausgangsgröße)
  - kann Konfigurationsregister haben
  - Beispiel Abstandssensor
    - Laufzeitmessung mit Ultraschall-Puls

### Analog/Digital-Wandler

- mögliche interne Funktionsweise: Sukzessive Approximation mit D/A-Wandler

[Analog/Digital-Wandler](/fom/semester-6/embedded-systems-iot-smartx/hardware.md#adc--analogdigital-converter-dac--digitalanalog-converter)

Fehlerarten:

- Quantisierungsfehler -> quantisierungsrauschen (digitalwert zu weit entfernt von echtem Wert)
- Nicht Linearität Fehler -> Abweichung der tatsächlichen AD-Wandler Kurve über den gesamten Messbereich
- Differential-Fehler -> Abweichung zweier aufeinander folgender Werte falsch
- Thermisches-Rauschen

## Aktoren

- beeinflusst die Umgebung
- bildet Stellglied im Regelkreis
- Setzt Steuersignale in mechanische Bewegung um
  - elektrisch
  - pneumatisch
  - hydraulisch
- Beispiele:
  - Ventile
  - Kolben
  - Motoren/Servos - Ansteuerung über PWM
