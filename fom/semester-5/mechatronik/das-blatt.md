---
title: Das Blatt
published: 1
date: 2023-12-11T19:29:37.207Z
tags: 
editor: markdown
dateCreated: 2023-12-11T19:29:37.207Z
---

# Das Blatt

## Einmassenschwinger

![Einmassenschwinger_Blatt](/fom/semester-5/mechatronik/Einmassenschwinger_Blatt.png)

### Definitionen

$F_T$ = Trägheitskraft  
$F_d$ = Dämpfungskraft  
$F_k$ = Federkonstante  
$F_A$ = Antriebskraft  
$F_G$ = Gravitationskraft  
$F_B$ = Beschleunigungskraft / Antriebskraft  
$m$ = Masse  
$d$ = Dämpfungskonstante  
$k$ = Federkonstante  
$p$ = Impuls  
$\dot{p} = e$ = effort  
$x = q$ = Auslenkung  
$\dot{x} = v = \dot{q} = \frac{p}{m} = f$ = Geschwindigkeit (flow)  
$\ddot{x} = \dot{v} = \ddot{q} = \dot{\frac{p}{m}}$ = Beschleunigung  

### Kräfte

$ \vec{0} = \vec{F_T} + \vec{F_d} + \vec{F_k} + \vec{F_A}$  

$0 = -m \vec{\ddot{x}} - d \vec{\dot{x}} - k\vec{x}+ \vec{F_A}$

$\vec{F_B} = \vec{F_A} + \vec{F_d} + \vec{F_k} $

### Differentialgleichung 2. Ordnung (2 Speicher)

$m \ddot{x} + d \dot{x} + kx = F_A$

oder

$m \ddot{x} = F_A - d \dot{x} - kx$

> $ \sum{\vec{F_i}} = \vec{0} $ Die Summe aller Kräfte ist Null
{.is-info}

> $ \vec{F_B} =  -\vec{F_T} $ Die Beschleunigungskraft entspricht der negativen Trägheitskraft
{.is-info}

### Blockschaltbild

2 Zustandsvariablen:

- $z_1 = x(t)$
- $z_2 = v(t) = \dot{x}(t) = \dot{z_1}$

$\dot{Z_2} = \ddot{x} = \frac{F_A}{m} - \frac{d}{m} * Z_2 - \frac{k}{m} * Z_1$

$\dot{x} = v$  
$\dot{v} = \frac{F_A}{m} - \frac{d}{m} * v + \frac{k}{m} * x$  

$\dot{q} $

![Einmassenschwinger_Blatt_BSB](Einmassenschwinger_Blatt_BSB.png)

### DGL 1.0 im Zustandsraum

![Einmassenschwinger_Blatt_Bond](Einmassenschwinger_Blatt_Bond.png)

## Schwingkreis
