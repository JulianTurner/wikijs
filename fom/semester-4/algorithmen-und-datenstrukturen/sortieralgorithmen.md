---
title: Sortieralgorithmen
published: 1
date: 2023-05-17T19:59:25.207Z
tags: 
editor: markdown
dateCreated: 2023-05-17T19:59:25.207Z
---

# Sortieralgorithmen

Sortieralgorithmen ordnen eine Menge von Elementen gemäß einer Sortierfunktion in eine bestimmten Reihenfolge

- Sortierfunktion -> Funktion deren Ergebnis die Reihenfolge der Elemente bestimmt
- Sortierschlüssel -> Argument der Sortierfunktion

- in-place Sortieralgorithmen -> Sortieren die Elemente ohne zusätzlichen Speicherplatz zu benötigen
- out-of-place Sortieralgorithmen -> Sortieren die Elemente mit zusätzlichem Speicherplatz

- stabil -> Elemente werden immer in der gleichen Reihenfolge sortiert
- instabil -> Elemente können in unterschiedlicher Reihenfolge sortiert werden

## Bubble Sort

- in-place
- stabil
- Zwei benachbarte Elemente werden verglichen und bei Bedarf getauscht
- Die größten Elemente werden nach und nach nach hinten verschoben
- Die tatsächliche Laufzeit ist abhängig von der Anzahl der Elemente und der Anzahl der Vertauschungen
- Die theoretische Laufzeit ist `O(n^2)`

```pseudo

for i = 0 to n - 1
    swapped = false
    for j = 0 to n - i - 1
        if a[j] > a[j + 1]
            swapped = true
            swap(a[j], a[j + 1])
    if swapped == false
        break
```

Vorteile:

- einfach zu implementieren
- schneller je näher die Liste bereits sortiert ist

Nachteile:

- langsam wenn die Liste stark unsortiert ist

## Selection Sort

## Heap Sort

## Merge Sort

## Insertion Sort

## Quick Sort

## Counting Sort

## Radix Sort
