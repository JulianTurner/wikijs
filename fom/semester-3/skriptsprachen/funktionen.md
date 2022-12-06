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

### Spezielle Parameter

- `/`: davor nur Positions-Argumente
- `*`: danach nur Keyword-Argumente

```python
def print_args(a, b, /, c, d, *, e, f):
    print(a, b, c, d, e, f)

print_args(1, 2, 3, 4, e=5, f=6)

# 1 2 3 4 5 6

print_args(1, 2, c=3, d=4, e=5, f=6)

# 1 2 3 4 5 6

print_args(1, 2, 3, 4, 5, 6)

# TypeError: print_args() takes 4 positional arguments but 6 were given

print_args(a=1, b=2, c=3, d=4, f=5, e=6)
# TypeError: print_args() got some positional-only arguments passed as keyword arguments: 'a, b'

```

> Spezielle Parameter sind optional
{.is-info}

### Call by value/reference

Call by reference:

- Mutable Objekte da diese verändert werden können

```python
def change_list(my_list):
    my_list.append(4)

my_list = [1, 2, 3]

change_list(my_list)

print(my_list)

# [1, 2, 3, 4]
```

> my_list wird als Parameter übergeben
{.is-info}

Call by value:

- Immutable Objekte da diese nicht verändert werden können

```python
def add_one(num):
    num += 1

my_num = 1

add_one(my_num)

print(my_num)

# 1
```

> Wert von my_num (1) wird als Parameter übergeben
{.is-info}

## Lambda-Funktionen & Closure

### Lambda-Funktionen

- Lambda-Funktionen sind anonyme Funktionen
- beliebig viele Parameter
- nur eine Operation

```python
add_one = lambda num: num + 1

print(add_one(1))

# 2
```

### Globale & lokale Variablen

- Globale Variablen sind in allen Funktionen verfügbar
- Lokale Variablen sind nur in Funktionen verfügbar

Beispiel:

```python
my_num = 1

def add_one(num):
    num += 1
    return num

print(add_one(my_num))

# 2

print(my_num)

# 1
```

Beispiel mit `global` Keyword:

```python
my_num = 1

def add_one():
    global my_num
    my_num += 1

add_one()

print(my_num)

# 2
```

> bei `global` ist Variable im globalen Scope in Funktion verfügbar
{.is-info}

Beispiel mit `nonlocal` Keyword:

```python
my_num = 5
def outer():
    my_num = 1

    def inner():
        nonlocal my_num
        my_num += 1

    inner()
    print(my_num)

outer()

# 2
```

> bei `nonlocal` muss die Variable zuvor in einem äußeren Scope (nicht global) definiert sein
{.is-info}

### Closure

- Closure ist ein Funktionsobjekt die auf eine Variable aus einem äußeren Scope zugreift
- ist nicht äquivalent zur Lambda Funktion
- Ausführung außerhalb des ursprünglichen Gültigkeitsbereichs
- ermöglichen Data-Hiding

```python
def outer(name):
    my_num = 1

    def inner():
        print(f'{name} + {my_num}')

    return inner

my_max_func = outer("Max")

my_max_func()

# Max + 1

my_sepp_func = outer("Sepp")

my_sepp_func()

# Sepp + 1
```

## Decorators

Syntaktischer Zucker um die Definition von Funktionen zu beeinflussen

dekorierende Funktion:

- erhält Original-Funktion als Parameter
- gibt neue Funktion zurück (Wrapped idr. Original-Funktion)

```python
def my_decorator(func):
    def wrapper():
        print("Before")
        func()
        print("After")

    return wrapper

@my_decorator
def my_func():
    print("Hello World")

my_func()

# Before
# Hello World
# After
```
