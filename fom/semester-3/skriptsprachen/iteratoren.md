---
title: Iteratoren
description: 
published: 1
date: 2022-10-14T11:23:05.735Z
tags: 
editor: markdown
dateCreated: 2022-10-13T12:49:44.966Z
---

# Iteratoren
Objekt welches Zustand der Iteration repräsentiert 

`iter()` & `next()`:
- mit `iter()` wird ein Iterator erzeugt
- mit `next()` wird der nächste Wert des Iterators zurückgegeben
- gibt Fehler wenn kein weiterer Wert vorhanden ist

```python
my_list = [1, 2, 3]
my_iter = iter(my_list)
next(my_iter)
1
next(my_iter)
2
next(my_iter)
3
next(my_iter)
Traceback (most recent call last):
StopIteration
```

## Enumerate
Gibt zu einem Collection-Objekt eine Enumerate-Objekt zurück


```python
my_list = [1, 2, 3]
my_iter = enumerate(my_list)
next(my_iter)
(0, 1)
next(my_iter)
(1, 2)
next(my_iter)
(2, 3)
```

## Generator
Jeder Generator ist ein Iterator, aber nicht jeder Iterator ist ein Generator
- Aufruf führt nicht direkt Code aus
- liefert Generator Objekt zurück
- verwenden `yield` 
    - hält Funktion an und liefer Wert zurück
    - beim nächsten Aufruf wird an der Stelle weitergemacht
- Trennung von Erzeugung und Verarbeitung (lazy evaluation)

```python
def my_generator(n):
    for i in range(n):
        yield i

my_gen = my_generator(3)
next(my_gen)
0
next(my_gen)
1
next(my_gen)
2
```



### Generator Expression
Analog zu List Comprehension  

```python
my_gen = (i for i in range(3))
next(my_gen)
0
next(my_gen)
1
next(my_gen)
2
```	

## Zip
Erzeugt Iterator dessen Elemente Tupel sind

```python
my_list1 = [1, 2, 3]
my_list2 = ['a', 'b', 'c']

my_zip = zip(my_list1, my_list2)
next(my_zip)
(1, 'a')
next(my_zip)
(2, 'b')
next(my_zip)
(3, 'c')
```

## Itertools
Bietet Hilfsfunktionen für Iteratoren

### count
Erzeugt unendlichen Iterator mit Startwert und Schrittweite

```python
import itertools

iterator = itertools.count(start=3, step=2)
next(iterator)
3
next(iterator)
5
next(iterator)
7
```

Gleiche ohne itertools:

```python
def count(start, step):
    while True:
        yield start
        start += step

iterator = count(3, 2)
next(iterator)
3
next(iterator)
5
next(iterator)
7
```

### cycle
durchläuft eine Collection endlos

```python
import itertools

iterator = itertools.cycle([1, 2, 3])
next(iterator)
1
next(iterator)
2
next(iterator)
3
next(iterator)
1
next(iterator)
2
next(iterator)
3
# ...
```

Gleiche ohne itertools:

```python
def cycle(collection):
    while True:
        for element in collection:
            yield element

iterator = cycle([1, 2, 3])
next(iterator)
1
next(iterator)
2
next(iterator)
3
next(iterator)
1
next(iterator)
2
next(iterator)
3
# ...
```

