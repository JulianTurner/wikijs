---
title: Systemtechnische Methodik
published: 1
date: 2023-10-11T19:46:54.207Z
tags: 
editor: markdown
dateCreated: 2023-10-11T19:46:54.207Z
---

# Systemtechnische Methodik

## Technisches System

- durch Funktion und Struktur verbunden
  - Systemstruktur -> Gesamtheit der Systemelemente und deren Beziehungen
  - Systemfunktion -> Überführung von operativer Eingangsgrößen in funktionelle Ausgangsgrößen
- durch Systemgrenze von Umwelt abgegrenzt

Zerlegung des Gesamtsystems:

```kroki
graphviz

digraph D {
  subgraph cluster_gesamtsystem {
    label = "Gesamtsysytem";
    subgraph cluster_teilsystem {
      label = "Teilsystem";
      subgraph cluster_subsystem {
        label = "Subsystem";
        subgraph cluster_systemkomponente {
          label = "Systemkomponente";
          Systemelement;          
        }
      }
    }
  }
}
```

### Input / Output

Eingangsgrößen:

- $X$ operative Größen (hat unmittelbaren Einfluss)
- $H$ Hilfsgrößen (nicht direkt am Prozess beteiligt, z.B. Spannung beim Arbeitskreis)
- $Z$ Störgrößen (z.B. //TODO)
- Dissipationseffekte (z.B. Umwandlung Energie in Wärme)

Ausgangsgrößen:

- $Y$ Funktionsgrößen (z.B. //TODO)
- $V$ Verlustgrößen (z.B. //TODO)
<!-- Seite 47 im Skript -->

> Funktion überführt Eingangsgrößen in Ausgangsgrößen
> Prozess Gesamtheit aller internen Vorgänge
{.is-info}
