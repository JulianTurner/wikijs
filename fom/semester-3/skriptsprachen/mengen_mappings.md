---
title: Mengen und Mappings
description: 
published: 1
date: 2022-10-14T11:23:05.735Z
tags: 
editor: markdown
dateCreated: 2022-10-13T12:49:44.966Z
---

# Mengen und Mappings

## Mengen / Sets
- ungeordnete Ansammlungen von Elementen, die keine Duplikate enthalten (eindeutig)
- Jedes Element muss unveränderlich sein (immutable => hashable)
- beliebige Werte-Datentypen
- 2 Typen:
    - `set` (mutable => Elemente können hinzugefügt und entfernt werden)
    - `frozenset` (immutable => Elemente können nicht hinzugefügt oder entfernt werden)

Erzeugung von `set`:
    - `set()`
    - `{1, 2, 3}` (mit Elementen)
    - `set([1, 2, 3])` (mit Elementen)

Erzeugung von `frozenset`:
    - `frozenset()`
    - `frozenset([1, 2, 3])` (mit Elementen)

Komplexität:
- `in`: O(1) (konstant)
- `add`: O(1) (konstant)
- `remove`: O(1) (konstant)

## Mappings / Dictionaries
- ungeordnete Ansammlung von Schlüssel-Wert-Paaren
- Schlüssel müssen unveränderlich sein (immutable => hashable)
- Schlüssel sind sortiert (ab Python 3.7)
- `dict` (mutable => Schlüssel-Wert-Paare können hinzugefügt und entfernt werden)
- beliebige Datentypen als Schlüssel und Werte
Erzeugung von `dict`:
    - `dict()`
    - `{}` (leeres Dictionary)
    - `{'a': 1, 'b': 2}` (mit Schlüssel-Wert-Paaren)
    - `dict([('a', 1), ('b', 2)])` (mit Schlüssel-Wert-Paaren)

Schlüssel können Iteriert werden:
```python
my_dict = {'a': 1, 'b': 2}
for key in my_dict:
    print(key)

# a
# b
```

Werte können Iteriert werden:
```python
my_dict = {'a': 1, 'b': 2}
for value in my_dict.values():
    print(value)

# 1
# 2
```

Schlüssel-Wert-Paare können Iteriert werden:
```python
my_dict = {'a': 1, 'b': 2}
for key, value in my_dict.items():
    print(key, value)

# a 1
# b 2
```

> Während Iteration können keine Elemente hinzugefügt oder entfernt werden
{.is-info}

Zuweisung von Werten:
```python
my_dict = {'a': 1, 'b': 2}
my_dict['c'] = 3
print(my_dict)

# {'a': 1, 'b': 2, 'c': 3}
```

Entfernen von Werten:
```python
my_dict = {'a': 1, 'b': 2}
del my_dict['a']
print(my_dict)

# {'b': 2}
```

Ersetzen von Werten:
```python
my_dict = {'a': 1, 'b': 2}
my_dict['a'] = 3
print(my_dict)

# {'a': 3, 'b': 2}
```

Werte finden:
```python
my_dict = {'a': 1, 'b': 2}
print(my_dict['a'])

# 1
```

Prüfen ob Schlüssel vorhanden:
```python
my_dict = {'a': 1, 'b': 2}
print('a' in my_dict)

# True
```

Komplexität:
- `in`: O(1) (konstant)
- `add`: O(1) (konstant)
- `remove`: O(1) (konstant)
- `get`: O(1) (konstant)

