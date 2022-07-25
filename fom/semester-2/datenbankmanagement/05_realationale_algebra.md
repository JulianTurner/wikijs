---
title: Relationale Algebra
description: 
published: 1
date: 2022-01-13T19:25:58.309Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:44:54.647Z
---

# Relationale Algebra

## Operatoren in Relationalen Algebra

$\sigma$ Selektion  
$\prod$ Projektion  
$\cup$ Union  
$-$ Differenz  
$\times$ Kreuzprodukt  
$\rho$ Umbenennung

$\bowtie$ Join  
$\ltimes$ Left-Join


## Selektion 

$\sigma_F(R)$  
Auswahl von Zeilen von R mit der Bedingung F  

Beispiel:  
Studenten > 10 Semester 

> $\sigma_{Semester > 10}(Studenten)$

## Projektion

$\prod_{A_i}(R)$  
Auswahl einer Menge von Spalten mit einer Relation
Duplikate werden eliminiert

Beispiel:  
Alle Rangbezeichnungen

> $\prod_{Rang}(Professoren)$


## Vereinigung

$R \cup S$  
Gibt Zeilen beider Tabellen aus

Beispiel:  
Name der Professoren und Assistenten

> $\prod_{Name}(Professoren) \cup \prod_{Name}(Assistenten)$


