---
title: Datenbank Server Installieren
description: Guide fürs Installieren eines Datenbankservers
published: 1
date: 2022-03-17T10:42:45.542Z
tags: 
editor: markdown
dateCreated: 2022-03-17T10:35:51.869Z
---

# Datenbank-Server auf eurem System installieren

## Grund-Idee

Die Container Software Docker dafür verwenden, Datenbank-Server auf eurem Computer bereitzustellen.
Vorteile:

- Container können einfach restlos gelöscht und neu erstellt werden, wenn neu neu anfangen werden soll
- Container sind einfach einzurichten – es gibt keinen Setup-Wizard bei dem irgendwelche falschen Einstellungen getroffen werden könnten
- Container sind Betriebssystem-Unabhängig und werden von vielen Menschen verwendet, d. h. jeder mit dem gleichen Image kann Probleme finden und an deren Lösung mitarbeiten. Die Chancen das Fehler in viel genutzten Images vorkommen sind gering.

## Docker Funktionsweise

Im Internet liegen sogenannte Docker **Images**. Dies sind praktisch aufgeteilte vollständige Installationen von Anwendungen.
Aufgeteilt heißt mithilfe von Ebenen wird beispielsweise das Betriebssystem (häufig Headless-Linux) getrennt von der Anwendung ausgeliefert, d. h. wenn Ihr mehrere Container mit dem gleichen Betriebssystem und unterschiedlicher Anwendungs-Software bestücken wollt, muss das Betriebssystem nicht erneut heruntergeladen werden.

Mithilfe dieser **Images** erstellt Docker **Container**. **Images** sind praktisch nur eine Blaupause, wie eine Installation aussehen könnte und mithilfe dieser **Images** könnt ihr eine beliebige Anzahl an **Containern** erstellen.
**Container** sind Bestandteile von Docker in denen tatsächlich logische Abläufe vorgehen, z. B. Web-Requests beantworten, irgendwas innerhalb des Containers berechnen, etc. - sprich alles was ein normaler Computer halt so kann.

Neben **Containern** erstellt Docker auch **Volumes**. Dies sind virtuelle Dateisysteme, in denen besonders wichtige Teile einer Anwendung abgespeichert werden können (Bsp. Daten einer Datenbank). Diese **Volumes** existieren getrennt von **Containern**, d. h. selbst wenn  **Container** gelöscht und neu erstellt werden, können die wichtigen Daten überleben.

Natürlich hat der Docker User die volle Kontrolle über Docker, d. h. es können nach belieben **Images** herunterladen werden, nicht mehr benötigte **Images** gelöscht werden, **Container** erstellt/gelöscht werden und **Volumes** erstellt/gelöscht/einem Container zuweisen/von einem Container entfernen werden.

Jeder **Container** hat auch einen Lifecycle-Status (Bsp: `Exited`, `Up`), d. h. nur weil ein **Container** existiert heißt dies nicht das er Funktionalität bereitstellt oder Systemressourcen (CPU-Leistung/Arbeitsspeicher) beansprucht.**Container** können nach Belieben gestartet und gestoppt.

## Docker Container Software installieren

Dafür einfach dem Betriebssystem-entsprechenden Guide auf <https://docs.docker.com/get-docker/> folgen.
Falls Ihr Fragen zur Installation auf Windows oder Linux habt kann ich gerne helfen - für macOS fehlt mir leider die Hardware, vielleicht kann da jemand anderes helfen.

Auf Windows/MacOS stellt die Docker Desktop GUI Anwendung den Docker Service bereit, auf Linux sollten die Dienste `docker.socket` und `docker.service` laufen.

## Datenbank Server installieren

Wenn Docker läuft können Datenbank-Server mit den folgenden Befehlen via Eingabeaufforderung/Kommandozeile installiert werden:

Die Funktionsweise der beiden Kommandos sind ähnlich:

1. `docker` ist die Anwendung die auf eurem PC installiert ist
2. `run` ist die Aufforderung einen neuen Container zu starten
3. `--name x` vergibt einen Namen für den neuen Container
4. `-e ...` setzt eine Umgebungsvariable in der neuen Container-Umgebung
5. `-p x:x` bindet den jeweiligen default Port des Datenbank-Servers der in dem Container genutzt wird an den Port des Host-Computers, damit von außerhalb des Containers auf den Datenbank Server zugegriffen werden kann
6. `-d` Starte den Container in "detached" Mode, d. h. die Eingabeaufforderung wird wieder freigegeben, der Container läuft im Hintergrund
7. `abcde:tag` Name des Images + Versions-Tag. Die hier verwendeten Images sind die offiziellen Images der jeweiligen Datenbankserver. Diese werden von Docker.io heruntergeladen sofern sie nicht auf dem Host-PC bereits vorhanden sind.

### MariaDB

```CLI
docker run --name mariadb -e MYSQL_ROOT_PASSWORD=mypass -p 3306:3306 -d docker.io/library/mariadb:10.7.3
```

Kommando von <https://mariadb.com/kb/en/installing-and-using-mariadb-via-docker/> genommen und angepasst.

Der Tag am Ende des Kommandos (`10.7.3`) entspricht der Version des zu verwendenden Images. Ihr könnt hier nach neueren Versionen suchen <https://hub.docker.com/_/mariadb?tab=tags> . Ich empfehle nicht das `latest` Tag zu verwenden, sondern ein Label mit einer echten Versionsnummer zu verwenden.

### PostreSQL

```CLI
docker run --name postgres -e POSTGRES_PASSWORD=mysecretpassword -p 5432:5432 -d docker.io/library/postgres:12.10
```

Kommando von <https://hub.docker.com/_/postgres> genommen und angepasst.

Der Tag am Ende des Kommandos (`12.10`) entspricht der Version des zu verwendenden Images. Ihr könnt hier nach neueren Versionen suchen <https://hub.docker.com/_/postgres?tab=tags> . Ich empfehle nicht das `latest` Tag zu verwenden, sondern ein Label mit einer echten Versionsnummer zu verwenden.

## Nach Datenbank Server Installation

Nach dem Starten der Container könnt Ihr die Datenbankserver verwenden.
<https://dbeaver.io/> (Open Source) oder <https://www.jetbrains.com/datagrip/> (kostenlos mit Studentenstatus) sind empfehlenswert fürs Interagieren mit den jeweiligen Servern.

### Login-Details

Ports sind die default Ports die ihr auch in den Kommandos ablesen könnt.

Für Mariadb ist der default Benutzername `root` und das Passwort wurde via Umgebungsvariable im Kommando auf `mypass` gesetzt
Für PostgreSQL ist der default Benutzername `postgres` und das Passwort wurde via Umgebungsvariable im Kommando auf `mysecretpassword` gesetzt.

Sicherheits-technisch sollte das soweit passen solange Ihr eine aktive Firewall habt und die entsprechenden Ports nicht in der Firewall für den Zugriff von extern freigebt.

## Sonstiges Docker Wissen (Befehle)

- `docker container ls -a` listet alle eure **Container**. Das `-a` nicht vergessen, ansonsten werden nur laufende **Container** gezeigt

- `docker container start CONTAINERNAME` startet den **Container** mit dem Namen `CONTAINERNAME`

- `docker container stop CONTAINERNAME` stoppt den **Container** mit dem Namen `CONTAINERNAME`

- `docker container rm CONTAINERNAME` entfernt einen **Container** mit dem Namen `CONTAINERNAME`. (Vor dem entfernen den **Container** stoppen)

- `docker image --help` Listet Befehle für das managen von **Images**.

- `docker logs CONTAINERNAME` - zeigt den Log eines **Containers** mit dem Namen `CONTAINERNAME` (hilfreich wenn man sehen möchte was der DB server gerade so macht)

- `docker system info` - gibt eine Übersicht über die Docker Installation
