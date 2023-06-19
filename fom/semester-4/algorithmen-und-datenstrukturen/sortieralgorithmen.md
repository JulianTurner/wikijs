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
- Die theoretische Laufzeit ist $O(n^2)$

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

- in-place
- instabil
- Das kleinste Element wird gesucht und an die erste Stelle getauscht
- Wiederholte Suche auf der restlichen unsortierten Teilliste
- Die theoretische Laufzeit ist $O(n^2)$

```pseudo
for startindex = 0 to a.size() - 1
    min = startindex
    for vergleichsindex = startindex + 1 to n - 1
        if a[vergleichsindex] < a[min]
            min = vergleichsindex
    swap(a[startindex], a[min])
```

Vorteile:

- einfach zu implementieren

Nachteile:

- langsam

## Heap Sort

- in-place
- instabil
- Die Elemente werden in einen Heap eingefügt
- Root-Element wird wiederholt entfernt und an den Anfang der sortierten Teilliste getauscht
- Die theoretische Laufzeit ist $O(n * log(n))$

```pseudo
heapify(KompletteListe)
for AnzahlSortierterElemente = 0 to KompletteListe.size() - 1
    swap(KompletteListe.[0], KompletteListe.[KompletteListe.size() - AnzahlSortierterElemente  - 1])
    heapify(KompletteListe.[0] bis KompletteListe.[KompletteListe.size() - AnzahlSortierterElemente  - 2])
```

Vorteile:

- schnell

Nachteile:

- in der Praxis teuer

## Insertion Sort

- in-place
- stabil
- Erstes Element der unsortierten Teilliste wird in die sortierte Teilliste eingefügt
- Die theoretische Laufzeit ist $O(n^2)$

```pseudo
for ersterIndexUnsortierteListe = 1 to KompletteListe.size() - 1
    key = KompletteListe[ersterIndexUnsortierteListe]
    letzterIndexSortierteListe = ersterIndexUnsortierteListe - 1
    while letzterIndexSortierteListe >= 0 and KompletteListe[letzterIndexSortierteListe] > key
        KompletteListe[letzterIndexSortierteListe + 1] = KompletteListe[letzterIndexSortierteListe]
        letzterIndexSortierteListe = letzterIndexSortierteListe - 1
    KompletteListe[letzterIndexSortierteListe + 1] = key
```

Vorteile:

- Datenmenge kann während des Sortierens wachsen (an Ende anfügen)
- schnell wenn die Liste bereits sortiert ist

Nachteile:

- Indizes müssen beachtet werden

## Merge Sort

- out-of-place
- stabil
- Die unsortierte Liste wird maximal zerlegt
- Je zwei Teillisten werden wiederholt zusammengeführt
- Die theoretische Laufzeit ist `O(n * log(n))`

```pseudo
mergeSort(KompletteListe)
    if KompletteListe.size() <= 1
        return KompletteListe
    else
        Mitte = KompletteListe.size() / 2
        LinkeTeilliste = mergeSort(KompletteListe[0] bis KompletteListe[Mitte - 1])
        RechteTeilliste = mergeSort(KompletteListe[Mitte] bis KompletteListe[KompletteListe.size() - 1])
        return merge(LinkeTeilliste, RechteTeilliste)

merge(LinkeTeilliste, RechteTeilliste)
    Ergebnis = []
    linkerIndex = 0
    rechterIndex = 0
    while linkerIndex < LinkeTeilliste.size() and rechterIndex < RechteTeilliste.size()
        if LinkeTeilliste[linkerIndex] <= RechteTeilliste[rechterIndex]
            Ergebnis.append(LinkeTeilliste[linkerIndex])
            linkerIndex = linkerIndex + 1
        else
            Ergebnis.append(RechteTeilliste[rechterIndex])
            rechterIndex = rechterIndex + 1
    
    while linkerIndex < LinkeTeilliste.size()
        Ergebnis.append(LinkeTeilliste[linkerIndex])
        linkerIndex = linkerIndex + 1

    while rechterIndex < RechteTeilliste.size()
        Ergebnis.append(RechteTeilliste[rechterIndex])
        rechterIndex = rechterIndex + 1
    
    return Ergebnis
```

Vorteile:

- Links und Rechts können parallel sortiert werden (Multithreading)
- schnell

Nachteile:

- out-of-place
- Komplexität

## Quick Sort

- in-place
- instabil
- Erstes Element der unsortierten Teilliste wird als Pivot gewählt
- Ordne die restlichen Elemente so, dass zuerst Elemente < Pivot und dann Elemente > Pivot stehen
- Tausche Pivot mit dem letzten Element der linken Teilliste
- Wiederhole das Verfahren für die linke und rechte Teilliste
- Die theoretische Laufzeit ist `O(n * log(n))`

```pseudo
quickSort(KompletteListe, start, ende)
    if start < ende
        pivot = partition(KompletteListe, start, ende)
        quickSort(KompletteListe, start, pivot - 1)
        quickSort(KompletteListe, pivot + 1, ende)

partition(KompletteListe, fromIndex, toIndex): // A, H
    pivot = KompletteListe[fromIndex] //25
    insertIndex = fromIndex // D
    for compareIndex in fromIndex + 1 to toIndex: // B - H
        if KompletteListe[compareIndex] < pivot: // true
            if compareIndex > insertIndex + 1 // true
                var temp = KompletteListe[insertIndex + 1] // 40
                KompletteListe[insertIndex + 1] = KompletteListe[compareIndex]
                KompletteListe[compareIndex] = temp
                insertIndex++
              else
                insertIndex = compareIndex
    KompletteListe[fromIndex] = KompletteListe[insertIndex]
    KompletteListe[insertIndex] = pivot
    return insertIndex
```

Vorteile:

- schnell
- multithreading möglich

Nachteile:

- instabil
- komplex zu implementieren

## Counting Sort

- out-of-place
- stabil
- Die Elemente werden gezählt und in ein Array geschrieben
- Die theoretische Laufzeit ist $O(n + range)$

```pseudo
countingSort(KompletteListe)
    min = max.int // 1
    max = min.int // 9
    for element in KompletteListe
        if element < min:
            min = element
         if element > max:
            max = element
    range = max - min + 1
    counter = new Array(range)
    for element in KompletteListe:
        counter[element-min]++
    writeIndex = 0
    for index, times in enumerate(counter): 
        currentElement = index + min
        for element in 1 to times
            KompletteListe[writeIndex++] = currentElement
```

Vorteile:

- lineares Laufzeitverhalten

Nachteile:

- Laufzeit hängt von der Größe des Wertebereichs ab
- Speicherbedarf hängt von der Größe des Wertebereichs ab

## Radix Sort
