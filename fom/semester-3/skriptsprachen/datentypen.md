---
title: Datentypen
description: 
published: 1
date: 2022-10-14T11:23:05.735Z
tags: 
editor: markdown
dateCreated: 2022-10-13T12:49:44.966Z
---

# Datentypen

## Numerische Datentypen
int - Integer (ganze Zahlen)
float - Gleitkommazahlen
complex - Komplexe Zahlen

Präfix für alternative Zahlensysteme (0x, 0o, 0b)

> Wertebereich bei `int` ist nicht eingeschränkt
{.is-info}

## Sequentielle Datentypen
str - Zeichenketten (immutable)  
list - Sequenz beliebiger Instanzen (mutable)  
tuple - Sequenz beliebiger Instanzen (immutable)
bytes - Sequenz von Bytes (immutable)
bytearray - Sequenz von Bytes (mutable)

Zugriff über Index möglich 

> `str`, `bytes` und `tuple` sind immutable, d.h. sie können nicht verändert werden
{.is-info}

## Slice
`[start:stop:step]`

## Strings 
- nicht veränderbar
- einfache oder doppelte Anführungszeichen

mit f-Strings können Strings formatiert werden
```python
name = "Max"
print(f"Mein Name ist {name}")
```

## Dunder Methoden
Double Underscore Methoden
- sollten nicht direkt aufgerufen werden
- sollten von Utility-Funktionen verwendet werden

[Beispiel einer eigenen Implementation](https://github.com/JulianTurner/skriptsprachen/blob/master/dunder.py)

## Hash
- bei nicht veränderbaren Sequenzen (immutable)
- verwendet die ID 

## List Comprehension
- Erzeugen von Listen mit for-Schleife innerhalb von eckigen Klammern

```python
liste = [x for x in range(10)]
# [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

## UTF-8
- Unicode Transformation Format
- 8-Bit Zeichenkodierung
- 1 Byte = 8 Bit
- Anzahl der führenden 1en im ersten Byte definiert die Anzahl der Bytes (1110xxxx = 3 Bytes)
- Flogebytes starten mit 10xxxxxx
- Bytes ohne Folgebytes sind ASCII-Zeichen: 0xxxxxxx
- x = Payload-Bit

## Memoryview
- Sicht auf binäre Daten im Speicher
- ermöglicht Zugriff auf binäre Daten ohne Kopieren