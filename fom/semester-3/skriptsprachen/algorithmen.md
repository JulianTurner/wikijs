---
title: Algorithmen
description: 
published: 1
date: 2022-10-14T11:23:05.735Z
tags: 
editor: markdown
dateCreated: 2022-10-13T12:49:44.966Z
---

# Algorithmen

## Korrektheit

Algorithmen sind korrekt, wenn sie für alle Eingaben das richtige Ergebnis liefern.

Möglichkeiten Zuverlässigkeit zu erhöhen:

- Software Engineering
- Programmierung
- Validation
- Verifikation

Partielle Korrektheit + Terminierung = Totale Korrektheit

> Mit Testen kann man die Korrektheit eines Programms nicht vollständig beweisen
{.is-warning}

### Funktionale / Imperative Korrektheit

Funktional:

- meist einfach zu beweisen (z.B. vollständige Induktion)

Imperativ:

- kein funktionaler Zusammenhang zwischen Eingabe und Ausgabe
- Berechnungsschritte können Seiteneffekte haben
- schwerer zu beweisen (z.B. Hoare-Kalkül)

## Komplexität

### Laufzeitanalyse

Messen der Laufzeit:

- abhängig von Ausführungsumgebung (Hardware, Betriebssystem, Compiler)
- abhängig von Parameterwerten
- gängige Methode

Zählen der Elementaroperationen:

- Addition, Zuweisung, Vergleich, Zugriff auf Datenstruktur
- geht in Hochsprache nicht da Maschinencode abstrahiert wurde

### Betrachtete Eigenschaften

- Eingabegröße
- Laufzeit
- Speicherverbrauch

### Asymptotische Laufzeit

- bei kleinen Eingaben ist die Laufzeit uninteressant
- wie verhält sich die Laufzeit bei großen Eingaben?

asymptotischen Laufzeit => das Zeitverhalten des Algorithmus für eine potenziell unendlich große Eingabemenge

> Es interessiert also nicht der Zeitaufwand eines konkreten Programms auf einem bestimmten Computer, sondern viel mehr, wie der Zeitbedarf wächst, wenn mehr Daten zu verarbeiten sind, also z. B. ob sich der Aufwand für die doppelte Datenmenge verdoppelt oder quadriert (Skalierbarkeit)
{.is-info}

### Schranken

- Schwer genaue Verteilung zu finden
- Worst-Case Betrachtung am interessantesten => Obere Schranke

Laufzeit für beliebige Eingabe $<=$ Obere Schranke  

### Big-O Notation

- beschreibt asymptotische Laufzeit und Komplexität
- beschreibt das Verhalten der Laufzeit sowie Speicherplatzbedarf (obere Schranke)
- beim Bestimmen zählt der am stärksten wachsende Summand (z.B. mit höchster Exponent)

- Kontakten sind unabhängig von Eingabe

Notation | Sprechweise | Beispiel
---|---|---
$O(1)$ | konstant | Addition von zwei Zahlen
$O(log n)$ | logarithmisch | Binäre Suche
$O(n)$ | linear | Durchsuchen eines Arrays
$O(n log n)$ |  | Gute Sortieralgorithmen
$O(n^2)$ | quadratisch | Primitive Sortieralgorithmen

> Bei kleinen Problemen (z.B. Dynamischer Programmierung) können Algorithmen mit schlechter asymptotischer Laufzeit besser sein
{.is-info}

## Rekursion vs. Iteration

Warum ist Rekursion ineffizient?

- Kette von Funktionsaufrufen führt zu wachsendem Call Stack (Speicherplatzbedarf)
- jeder Funktionsaufruf arbeitet in eigener lokaler Umgebung

Beispiel:

```python
def fib(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fib(n-1) + fib(n-2)
```

> Python hat eine maximale Rekursionstiefe
{.is-warning}

### Lineare Rekursion

- jeder Zweig hat maximal einen rekursiven Aufruf

```python
def f(n):
    result = -1
    
    if n == 0:
        result = 0
    else:
        result = 1 + f(n-1)
    
    print(result)
    return result
```

### Endrekursion

- Lineare Rekursion mit einem einzigen rekursiven Aufruf am Ende
- keine weiteren Operationen nach dem rekursiven Aufruf
- es müssen keine Zwischenergebnisse gespeichert werden
- kann einfach in eine Iteration umgewandelt werden
- nicht alle rekursiven Algorithmen sind endrekursiv umsetzbar

```python
def f(n, a):
    if n == 0:
        return a
    else:
        return f(n-1, a+1)
```

> Endrekursion wird in Python nicht optimiert
{.is-warning}

### Dynamische Programmierung

Memoisierung:

- Rekursion mit Memoisierung
- Zwischenergebnisse werden gespeichert
- nur einmal berechnet
- nur bei endrekursiven Algorithmen möglich

Beispiel mit LRU-Cache:

```python
from functools import lru_cache

@lru_cache(maxsize=None)
def fib(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fib(n-1) + fib(n-2)
```

Tabularisierung:

- Iteration mit Tabularisierung
- Zwischenergebnisse werden gespeichert
- nur einmal berechnet
- nur bei endrekursiven Algorithmen möglich

Beispiel:

```python
def fib(n):
    fibs = [0, 1]
    
    for i in range(2, n+1):
        fibs.append(fibs[i-1] + fibs[i-2])
    
    return fibs[n]
```
