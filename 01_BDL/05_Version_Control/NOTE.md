# Versionskontrollsystem

- Während der Softwareentwicklung entstehen verschiedene Versionen
- Systeme, die dabei helfen,
  - dass an mehreren Versionen eines Projekts
  - dass mehrere Personen an einem Projekt arbeiten können
  - dass der Code überprüft werden kann

## Git

- das gängiste Versionskontrollsystem
  - ~50 Jahren

> Commit = Sammlung von Änderungen die bereit sind

### Befehle

- Überprüfung der Version
  - `git --version`

- Den Status der `staged` Dateien einsehen
  - `git status`

- Unterschiede in den Änderungen
  - `git diff`

- Initialisierung eines git-Projekts
  - `git init`

- Dateien sind zuerst in einem nicht erfassten Zustand = `untracked` vorgemerkt werden
  - `git add .`, Dieser Befehl erfasst alle Änderungen im momentanem Verzeichnis
  - `git add <datei>`, Dieser Befehl fügt eine bestimmte Datei in den "Zwischenspeicher" ein
  - Danach sind die Dateien in einem sogenannten `staged` Zustand

- Jetzt sind die Dateien bereit, committed zu werden.
  - Alle Dateien, die sich im `staged` Bereich befinden
  - `git commit -m ""`
  - Zuerst wird das lokale Repository den Commit speichern
  
- Klonen eines Git-Repositories
  - `git clone <git-repository>`
  - Das Repository ist in einer Cloud gespeichert

- Änderungen hochladen
  - `git push`

- Änderungen herunterladen
  - `git pull`
  - Das Repository muss in einem sauberen Zustand vorhanden sein
    - Offene Änderungen müssen entweder committed oder gestashed werden oder ungewollte Änderungen müssen zurückgesetzt werden

- Alle Dateien werden in den Ursprungszustand zurückgesetzt
  - `git restore .`

