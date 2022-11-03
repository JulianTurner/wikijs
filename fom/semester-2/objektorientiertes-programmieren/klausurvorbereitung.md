---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-03-05T08:33:57.107Z
tags: 
editor: markdown
dateCreated: 2022-03-04T12:23:08.923Z
---

# Klausurvorbereitung

# Skipt 1

## Was ist das Hauptziel der Entwicklung von Java?

- Entwicklung vollständiger Betriebssystementwicklung
- inkl. virtuelle CPU
- unterschiedliche Einsatzzwecke

## Wesentliche Ziele der Java-Technology?

- Plattforunabhängigkeit

1. Quellcode in Bytecode kompiliert
1. auf Zielsystem von der JRE
	- in Maschienensprache übersetzt
	- ausgeführt

> Bytecode ist Zwischencode zwischen Programmiersprache und Maschinensprache

> für jedes ausführende Gerät muss eine passende JRE installiert sein

## Was ist der Unterschied zwischen JDK und JRE?

JDK enthält JRE

- JDK enthält Entwicklertools wie Compiler, Debugger, Profiler, etc.
JRE enthält nur die Laufzeitumgebung

# Skript 4

## Was ist ein Algorithmus?

- eindeutige Handlungsvorschrift zur Lösung eines Problems
- besteht aus endlich vielen Einzelschritten

## Was ist = ?

ein Zuweisungsoperator

# Skript 5

## Was ist ein einfacher Datentyp?

- nicht weiter zerlegbar (atomar)
- vordefinierter Standardtyp
- primitives in Java
- haben keine Methoden
- nicht als Klasse realisiert

## Was ist eine Klasse?

Verbund von Daten und Methoden

# Skript 6

## Worum geht es bei OOP?

- Objekte / Dinge / Konzepte der realen Welt zu beschreiben
- miteinander ein Programmsystem bilden
- durch Zusammenwirken ein Problem lösen

## Was sind Objekte?

- Instanzen von Klasse
- Beschreiben die wesentlichen Aspekte

## Was sind Klassen?

- Klassen stellen allgemeine Baupläne für Objekte dar
- werden von realen Objekten abstrahiert
- haben einen Namen, Datenfelder, Methoden
- sind wie Datentypen zu verwenden
- werden zu Laufzeit für die Erzeugung von Objekten verwendet

## Start für ein Java-Programm?

```java
public class Main {
	public static void main(String[] args) {
			//System.out.println("Hello World!");
		}
	}
```

## Wann verwendet man den new-Operator?

Um ein neues Objekt zu erzeugen

- wickelt die Speicherreservierung im Heap ab

# Skript 7

Was ist Abstraktion?

- auf das wesentliche konzentrieren
- komplexe Zusammenhänge, Dinge vereinfachen

## Was bedeutet Kapselung?

- Objekt besteht aus Daten und Methoden als eine Einheit
- Objekt verwaltet seine Daten selbst
- soll ein Objekt seine Daten ändern muss es Methoden aufweisen
- Methoden können von anderen Objekten aufgerufen werden
- Methoden die von anderen Objekten aufgerufen werden können sind Schnittstellenmethoden

## Was ist Information Hiding?

- nach außen sichtbare Methoden sind ``public``
- nach innen sichtbare Methoden sind ``private``
  - versteckt inneres Verhalten

## Was gilt in OOP grundsätzlich?

- Programme basieren auf Klassen aus dene Objekte zu Laufzeit erzeugt werden
- Objekte leben im Heap (Teil von RAM)
- Objekte haben Daten und Methoden
- Methoden haben automatisch Zugriff auf alle Datenfelder des Objekts
- Methoden dienen dazu Datenfelder eines Objekts zu verwalten & verändern
- Datenfelder sind i.d.R. ``private```

## Was sind Datenfelder?

- legen Zustand des Objekts fest
- Zustand wird durch Methoden verändert

## Was sind Methoden?

- bewirken Zustandsänderungen
- geben Werte aus

## Was sind Objekt und Klassendiagramme?

![](objekt-klassendiagramm.png)  
Oben = Objektdiagramm  
Unten = Klassendiagramm  

## Vererbungshierarchie

![](Vererbungshierarchie.png)

# Skript 10

## final

- final Instanzvariable kann nach Instanzsierung nicht geändert werden
- final Klassenvariable kann kein anderer Wert zugewiesen werden
- final Methode kann nicht überschrieben werden
- final Klasse kann nicht geerbt werden

# Skript 11

## Primitive Datentypen

- aus performace Gründen nicht als eigene Klasse implementiert
- Wrapper Klassen für zusätzliche Funktionen
- wenn nicht Feld von Objekt dann auf dem Stack

## Referenzdatentypen

- konstrukte um aus primitiven Datentypen eigene Typen zu erzeugen
- Zugriff nur indirekt über Referenz

## Referenzvariablen

- stellen Verknüpfung zu einem Objekt dar
- ermöglichen Zugriff auf Objekte über Referenz

Bei Instanz- Klassenvariable erfolgt Initialisierung mit default Werten.
Lokale Variable muss selbst initialisiert werden.

> Objekte ohne Referenzvariablen werden im Garbage Collector freigegeben.

## Wo liegen Objekte von Referenzvariablen?

- Klassenvariable (static) in der Method Area
- Instanzvariablen im Heap
- lokale Variablen im Stack

## Was kommt zuerst? Klasse oder Objekt?

zuerst Klasse, dann Objekt
da Objekt Instanz einer Klasse

# Skript 14

## Was macht die this-Referenz?

- Referenz auf das aktuelle Objekt

## this Anwendungsfälle

- Datenfelder haben den selben Namen wie Übergabeparameter (häufig im constructor, spart neue Namen)
- Darstellung dass auf eine Instanzvariable/-methode des aktuellen Objekts verwiesen wird
- Rückhabe einer Referenz auf das aktuelle Objekt

# Skript 15

## Was ist Methoden Überladung?

- Methoden mit selebn Namen aber unterschiedlichen formalen Parametern

## Was ist eine Sigantur?

Methodenname + formale Parameter

## Wie werden Objekte zur Laufzeit erstellt?

```java
Class b;         // Deklaration
b = null;        // Initialisierung
b = new Class(); // Instanzierung
```

> Konstruktoren haben die selben Namen wie die Klasse

## init Klassenvariable

```java
class Klasse {
	static int zahl;  // 0 wenn nicht initialisiert

	static {
		zahl = 10;
	}
}
```

## init Instanzvariablen

```java
class Klasse {
	int zahl;

	{
		zahl = 10;
	}
}
```

## Was zeichnet einen Konstruktor aus?

- selber Name wir Klasse
- wird bei Erzeugung des Objektes ausgeführt
- Inistalizierungsroutine
- kein Rückgabewert
- wird nicht vererbt
- mehere Konstruktorern mit unterschiedlichen formalen Parametern

> Default Konstruktor ist der no Args Konstruktor

## Was zeichnet den default Konstruktor aus?

- keine Parameter
- wird automatisch definiert
- nicht mehr verfügbar wenn ein Konstruktor definiert wurde

# Skript 16

## Assoziation

- Beziehung zwischen Objekten
![](https://p7x7q5i4.rocketcdn.me/wp-content/uploads/2018/12/assoziation-1080x346.jpg)

## Komposition

- muss vorhanden sein  
![](https://p7x7q5i4.rocketcdn.me/wp-content/uploads/2019/01/komposition.jpg)

## Aggregation

- kann vorhanden sein  
![](https://p7x7q5i4.rocketcdn.me/wp-content/uploads/2020/03/uml-aggregation-wissen-kompakt.jpg)

## Wozu ist Vererbung gut?

- Wiederverwendung von Code
- Eigenschaften und Verhaltensweisen auf andere Klassen übertragen
- Hierachien aufbauen
- Modularisierung

# Skript 17

## Wann ist eine Klasse polymorph?

1. Oberklasse
1. Kinderklasse
1. Kindklasse tritt in gestalt der Oberklasse auf

# Skript 18

## Wofür brauche ich Exceptions?

zur strukturieten Ausnahmebehandlung

> Wenn die Exception nicht gecatched wird, wird sie zur nächsten Exception weitergereicht

## Wo ist der Unterschied zwischen Checked und UnChecked Exceptions?

Checked Exception:

- muss behandelt werden
UnChecked Exception:
- wird nicht behandelt

> Alle Exceptions bis auf Error und Runtime sind Checked Exceptions
> UnChecked Exceptions beenden das Programm

![](https://images-ext-1.discordapp.net/external/kbH3gpY0TGSZBE7NA73u2xPE2wQjgvAeePgTINXCUAI/https/lh5.googleusercontent.com/WqqNoyFEkZXfmZBBQjgIutY72_BUV6_By_BAe7Ih9u36HfelS3nTWQEYtdRUkQS32Tuhg9P9CUXo-jgvOpkO84vLm2viI4Od0BNustwONdMm7DKZnKC6kyVHyRJbsESLIPV4uBU?width=810&height=280)
