---
title: Python Basics
description: 
published: 1
date: 2022-10-13T14:16:11.354Z
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

IDEs mögen in diesem Fall eine Warnung im Code anzeigen, da die Funktion `add_b` mit `: A` eine Annotation am Parameter enthält, welche darauf Hinweist das `my_obj` vom Typ `A` sein sollte, aber ausführen lässt sich der Code komplett ohne Fehler oder Warnungen.

Objekte vom Typ `B` haben nie etwas von Objekte vom Typ `A` mitbekommen, sie erben nicht von `A` und stehen auch sonst in keinerlei Beziehung zu `A`.

Dies ist möglich, da Objekte vom Typ `B` ebenfalls ein Attribut `own_letter` besitzen.


## Veränderlichkeit

Mutable (Veränderbar): 
- Listen (`list`)
- Mengen (`set`)
- Wörterbücher (`dict`)
- Byte-Felder (`bytearray`)

Immutable (Nicht Veränderbar): 
- Nummerisch (`int`, `float`, `complex`, `bool`)
- Zeichenketten (`str`)
- Tupel (`tuple`)
- Mengen (`frozenset` - nicht verwechseln mit mutierbarem `set`)
- Bytes (`bytes`)

## Vergleiche

- `a == b` -> (Wertmäßige) Gleichheit
- `a is b` -> Referenzielle Gleichheit (äquivalent zu `id(a) == id(b)`

```python
a = [1, 2, 3]
b = a
c = a[:]  # erstellt eine neue Liste die alle Elemente von a enthält

print(a == b)  # Vergleiche Wert der zwei Objekte -> True
print(a is b)  # Vergleiche ob Objekte an gleicher Speicheradresse/gleiche Id -> True
print(a == c)  # Vergleiche Wert der zwei Objekte -> True
print(a is c)  # Vergleiche ob Objekte an gleicher Speicheradresse/gleiche Id -> False
```

> Python verwendet für Integer im Bereich -5 <= x <= 256 für Performance-Verbesserungen Singletone-Instanzen (wird nur ein mal Speicher für den gleichen Wert reserviert, egal wie vielen Variablen man den gleichen Wert zuweist). `is` Vergleiche von zwei Objekten mit dem gleichen Wert aus diesem Wertebereich werden `True` ergeben, während ein `is` Vergleich von zwei Variablen denen beispielsweise `1000` zugewiesen wurde `False` ergibt.
{.is-warning}

> `None` ist ebenfalls eine Singletone-Instanz -> `is` Vergleiche zweier Variablen denen `None` zugewiesen wurde ergibt `True`.
{.is-info}

## None

- Pythons Version von `Null` Werten
- Nicht equivalent zu `0` oder `False` (eigener Datentyp `NoneType`)
- None ist `falsey´ (wird `None` im Kontext eines boolischen Ausdrucks verwendet, wird es zu `False` ausgewertet)


