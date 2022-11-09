---
title: Funktionen
description: 
published: 1
date: 2022-10-14T11:23:05.735Z
tags: 
editor: markdown
dateCreated: 2022-10-13T12:49:44.966Z
---


# Funktionen

Funktion:

- Beinhaltet Anweisungen & gibt Wert mit `return` zurück
  - ohne `return` wird `None` zurückgegeben
- kann Argumente entgegennehmen

## Funktionsdefinition erzeugen ein Objekt

```python

def is_odd(num):
    return num % 2

print(type(is_odd))

# <class 'function'>

print(id(is_odd))

# 1400000000000

```

> Wenn Funktion wie Variable behandelt wird, spricht man von **First-Class-Functions**
{.is-info}

## Funktionsparameter

![Funktionsparameter](/fom/semester-3/skriptsprachen/funktionen/funktionsparameter.png)

1. Default-Argumente Stehen hinter Nicht-Default-Argumenten
1. Keyword-Argumente stehen hinter Positions-Argumenten
1. Alle Keyword-Argumente, die beim Funktionsaufruf übergeben werden, müssen einem Argument, das von der Funktion akzeptiert wird, entsprechen. Die Reihenfolge ist dabei unwichtig
1. Kein Argument darf beim Funktionsaufruf mehr als einen Wert zugewiesen bekommen
1. Default-Argumente Sind optionale Argumente

### Variable Anzahl an Argumenten

#### Postions-Argumente

```python
def sum(*args):
    result = 0
    for arg in args:
        result += arg
    return result

print(sum(1, 2, 3, 4, 5))

# 15

print(sum(1, 2, 3, 4, 5, 6, 7, 8, 9, 10))	

# 55

```

#### Keyword-Argumente

```python
def print_kwargs(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_kwargs(a=1, b=2, c=3)

# a: 1
# b: 2
# c: 3

print_kwargs(d=4, e=5)

# d: 4
# e: 5

```

### Argumente Auspacken

Beispiel mit `*args` und `list`:

```python
def print_args(*args):
    for arg in args:
        print(arg)

print_args(1, 2, 3, 4, 5)

# 1
# 2
# 3
# 4
# 5

my_list = [1, 2, 3, 4, 5]

print_args(*my_list)

# 1
# 2
# 3
# 4
# 5

```

Beispiel mit `**kwargs` und `dict`:

```python

def print_kwargs(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_kwargs(a=1, b=2, c=3)

# a: 1
# b: 2
# c: 3

my_dict = {"a": 1, "b": 2, "c": 3}

print_kwargs(**my_dict)

# a: 1
# b: 2
# c: 3

```

> `*` erwartet eine Liste, `**` erwartet ein Dictionary
{.is-info}
