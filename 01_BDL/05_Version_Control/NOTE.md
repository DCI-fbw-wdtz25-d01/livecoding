# Versionskontrollsystem

- Während der Softwareentwicklung entstehen verschiedene Versionen
- Systeme, die dabei helfen,
  - dass an mehreren Versionen eines Projekts
  - dass mehrere Personen an einem Projekt arbeiten können
  - dass der Code überprüft werden kann

## Git

- das gängiste Versionskontrollsystem
  - ~50 Jahren

- Initialisierung eines git-Projekts
  - `git init`
- Dateien sind zuerst in einem nicht erfassten Zustand = `untracked` vorgemerkt werden
  - `git add .`, Dieser Befehl erfasst alle Änderungen im momentanem Verzeichnis
  - Danach sind die Dateien in einem sogenannten `staged` Zustand
- Jetzt sind die Dateien bereit, committed zu werden.
  - Alle Dateien, die sich im `staged` Bereich befinden
  - `git commit -m ""`

> Commit = Sammlung von Änderungen die bereit sind
