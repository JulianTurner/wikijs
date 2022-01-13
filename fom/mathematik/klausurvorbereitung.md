---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-01-13T11:39:22.534Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:44:54.647Z
---

# Klausurvorbereitung

## Grundlagen

### Was ist eine Primzahl?
- Eine Primzahl kann man nur durch sich selbst oder 1 teilen z.b. { 3, 5, 7 }


### Aussagen
Eine Aussage beinhaltet keine Variable.
- morgen ist Sonntag = keine Aussage da morgen eine Variable ist
- nach Montag kommt Sonntag = aussage

### Mengen 
- die leere Menge ist in jeder Menge vorhanden
- eine Schnittmenge ist eine Menge die in der Menge $A$ und $B$ vorhanden ist. 

#### Addition von Mengen
$|A \cup B| = |A| + |B| - |A \cap B|$
> Bei Mengen gilt es zu Beachten die Schnittmenge bei Vereinigungen abzuziehen da sie sonst doppelt vorhanden wäre.

### Äquivalenzrelationen

Was ist reflexsiv?
- Ich habe am slelben Tag Geburtstag wie ich
- $500g \Leftrightarrow 500g$
>  Wenn $x$ in relation zu sich selbst steht
$x \thicksim x$
{.is-info}


Was ist symetrisch?
- Ich habe am selben Tag Geburtstag wie mein Zwilling.
- $1/2 kg \Leftrightarrow 500g$
> Wenn $x$ in Relation zu $y$ steht, dann steht $y$ auch in Relation zu $x$
$x \thicksim y \Leftrightarrow y \thicksim x$
{.is-info}


Was ist transitiv?
- der zwite drilling hat am selben Tag Geburtstag wie der dritte Drilling und ich habe am selben Tag Geburtstag wie der dritte Drilling.
- $0,5kg \thicksim 1/2 kg \land 1/2 kg \thicksim 500g \implies 0,5kg \thicksim 500g$
> Wenn x in Relation zu $y$ steht ***und*** $y$ in Relation zu $z$, dann steht auch $x$ in Relation zu $z$ 
$x \thicksim y \space \land y\thicksim z \implies x \thicksim z$ 
{.is-info}


### Abbildungen

Wann ist eine Abbbildung sujektiv?
- $x:\N, y:={2}$
> Wenn jedes Element in $y$ mindestens 1x getroffen wird
{.is-info}


Wann ist eine Abbbildung injektiv?
> Wenn ein Element in $y$ maximal 1x getroffen wird
{.is-info}

Wann ist eine Abbbildung bijektiv?
> Wenn die Abbildungeng sowohl sujektiv als auch injektiv ist
{.is-info}

# Algebraische Strukturen und Zahlenmengen
### Vollständige Induktion
- Beweisen der Bernouli-Ungleichung für $h \in \R$
$\forall n \in \N:(1+h)^n  \geq 1+nh, falls \space h \geq -1$

Infuktionsanfang: $n = 1$
|-|-|
| $(1+h) \geq 1+1*h$ | *Klammern auflösen da nicht benötigt*
| $1+h \geq 1 + 1*h$ | $* 1$ *entfernen*
| $1+h \geq 1 + h$ | $\square$

Induktionsbehauptung
$\exists n \in \N : (1+h)^n \geq 1+ nh, falls h \geq -1$

Induktionsschritt:
- zu zeigen $n \rightarrow n +1$
|-|-|
|$(1+h)^{n+1} \geq 1 + (n+1)h$| linke Seite Qutienten aufteilen
|$(1+h)^n * (1+h)^1 \geq 1 + (n+1)h$