---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-10-14T11:23:05.735Z
tags: 
editor: markdown
dateCreated: 2022-10-13T12:49:44.966Z
---


# Klausurvorbereitung

## Basic

### Welche Paradigmen verwendet Python?

- Prozedural
- Objektorientiert
- Imperativ

### Was ist der Unterschied zwischen Compiler und Interpreter?

- Compiler übersetzt Programm in Maschinensprache und erstellt ausführbare Datei
- Interpreter sucht nach passenden vorkompilieren Maschinencode und führt diesen aus

### Was ist der Unterschied zwischen statischer und dynamischer Typisierung?

- statische Typisierung: Typen werden bei der Übersetzung festgelegt
- dynamische Typisierung: Typen werden zur Laufzeit festgelegt

### Was ist der Unterschied zwischen starker und schwacher Typisierung?

- starke Typisierung: bei inkorrekter Typzuweisung wird ein Fehler geworfen
- schwache Typisierung: bei inkorrekter Typzuweisung wird der Typ automatisch konvertiert

### Wie kann man Seiteneffekte verhindern?

- z.B. mit Immutables
- mit pure Funktionen
- mit funktionaler Programmierung

### Was ist None?

- None ist ein Objekt, welches als Platzhalter für leere Objekte dient
- None ist ein Singleton
- Standardwert wenn kein Rückgabewert erwartet wird

### Was ist ein Generator?

- ein iterierbares Objekt
- erzeugt Werte erst auf Anfrage

### Wann ist der `in` Operator effizient?

- bei gehashten Kollektionen (z.B. Sets, Dictionary, FrozenSet)

### Was ist `enumerate`?

- gibt Index und Wert eines iterierbaren Objekts zurück
- ist ein Iterator

### Was ist `zip`?

- gibt Tupel aus iterierbaren Objekten zurück

### Wie entpackt man Tupel?

- mit `*` / splat Operator
- mit destructuring

### Was sind die Eigenschaften von einem `Set`?

- keine Duplikate (immutable)
- keine Reihenfolge
- `in` Operator in $O(1)$

### Was sind die Eigenschaften von einem `Dictionary`?

- Key-Value Paare
- keine Duplikate bei den Keys (immutable)
- Werte sind veränderbar (mutable)
- keine Reihenfolge
- `in` Operator in $O(1)$

### Was sind Lambda Funktionen?

- anonyme Funktionen
- können nur einen Ausdruck enthalten
- geben immer einen Wert zurück

### Was sind Closures?

- Funktionsobjekt welche an eine Umgebung gebunden ist

### Was sind Decorator?

- Funktionen welche andere Funktionen als Parameter entgegennehmen
- Geben neue Funktionen zurück

### Was ist der Unterschied zwischen `Global` und `Nonlocal`?

- die Ebene der Variable

### Was ist Endrekursion?

- Funktionsaufruf ist letzte Operation in der Funktion
- System muss zurück springen und zwischenspeichern

### Was ist der Unterschied zwischen Generator und List Comprehension?

- List Comprehension erzeugt eine Liste
- Generator erzeugt ein Generator Objekt, und liefert keine Werte bis er nicht konsumiert wird
- Runde Klammern bei Generator Expression
- Eckige Klammern bei der List Comprehension

#### Warum ist der in-Operator in Sets deutlich schneller als in Listen?

- in-Operator sucht linear in Listen durch iteration
- in-Operator sucht in Sets mit einer Hash-Operation (möglicher Index kann direkt berechnet werden)

## Algorithmen

### Warum ist Rekursion ineffizient?

- Kette von Funktionsaufrufen führt zu wachsendem Call Stack (Speicherplatzbedarf)
- jeder Funktionsaufruf arbeitet in eigener lokaler Umgebung

## Reguläre Sprachen

### Wofür verwendet man regEx?

- für die Suche nach Mustern in Texten
- für die Validierung von Eingaben
