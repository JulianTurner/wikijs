---
title: Python Basics
description: 
published: 1
date: 2022-10-13T12:56:04.294Z
tags: 
editor: markdown
dateCreated: 2022-10-13T12:49:44.966Z
---

# Python Basics

## Operationen

Operation | Bedeutung
---|---
`+`| Plus
`-`| Minus
`*`| Mal
`/`| Geteilt
`//`| Ganzzahldivision
`%`| Modulo
`**`| Potenz
`<<`| Arithmetische Verschiebung Links
`>>`| Arithmetische Verschiebung Rechts
`&`| Bitwise AND
`|`| Bitwise OR
`^`| Bitwise XOR
`~`| Bitwise NOT

## Ausgabe

```python
print('Die Antwort ist 42')
```

- Ausgabe mit der `print` Funktion
- Einfache Strings können mit einfachen oder doppelten Anführungszeichen übergeben werden


## Mehrzeilige Anweisungen (Beispiel if-Block)

```python
if answer == 42:
    print('Die Antwort ist 42')
```

- Bedinung muss nicht in Klammern gesetzt werden
- Doppelpunkt ist zwingend notwendig
- Alles was im Block steht muss eingerückt werden.

## Eingaben


```python
eingabe = input('Mache eine Eingabe')
print(eingabe)
```