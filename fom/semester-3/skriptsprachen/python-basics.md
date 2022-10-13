---
title: Python Basics
description: 
published: 1
date: 2022-10-13T13:26:32.183Z
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

- Bedingung muss nicht in Klammern gesetzt werden
- Doppelpunkt ist zwingend notwendig
- Alles was im Block steht muss eingerückt werden.

## Eingaben


```python
eingabe = input('Mache eine Eingabe')
print(eingabe)
```

## String zu Nummer Konvertierung

Verwende Konstruktoren `int(...)`, `float(...)`, `complex(...)` für die Konvertierung von Text zu Integern, Float-Zahlen und komplexe Zahlen.

## Variablen

- Alles außer Schlüsselwörter sind in Python Objekte
- Variablen denen Objekte zugewiesen werden können ohne Schlüsselwort einfach verwendet werden
- Objekte haben Zustand (state) und können (möglicherweise) verändert werden (mutation)

```python
a = 1
b = 2
a = 'auto`
```

Objekte werden im Speicher mit einer generierten Id, der zugewiesenen Value und einem Typ abgelegt.

## Duck Typing

Solange ein Objekt die benötigten Methoden/Attribute hat, kann es in einem Szenario verwendet werden, welches ursprünglich gar nicht für diesen bestimmten Objekttyp vorgesehen war.

Schreibt beispielsweise ein Bibliothek-Author folgenden Code:

```python 
class A:
    def __init__(self):
        self.own_letter = 'a'


def add_b(my_obj: A):
    return my_obj.own_letter + 'b'


if __name__ == '__main__':
    a_obj = A()
    print(add_b(a_obj))  # gibt den String 'ab' aus
```

kann ein Verwender der Bibliothek der Funktion `add_b` ein Objekt mit einem anderen Typen übergeben:

```python
class B:
    def __init__(self):
        self.own_letter = 'b'


if __name__ == '__main__':
    b_obj = B()
    print(add_b(b_obj))  # gibt den String 'bb' aus
```

IDEs mögen in diesem Fall eine Warnung im Code anzeigen, da die Funktion `add_b` mit `: A` eine Annotation am Parameter enthält, welche darauf Hinweist das `my_obj` vom Typ `A` sein sollte, aber ausführen lässt sich der Code komplett ohne Fehler oder Warnnungen.

Dies ist möglich, da Objekte vom Typ `B` ebenfalls ein Attribut `own_letter` besitzen.




