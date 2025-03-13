# Tastenbefehle
---
- `CTRL + L`/ => Reinigt den Bildschirm, setzt den Leiste oben an
- `CTRL + C` => Bricht einen Befehl ab, zB. wenn man sich in der Standardeingabe befindet
- `CTRL + D` => Signalisiert das Ende einer Eingabe

# Text-Befehle
---
- `clear`: 
	- Abhängig vom Betriebssystem wird die Befehlhistorie gelöscht, ansonsten wird nur der Bildschirm freigemacht
- `echo`: Gibt eine Eingabe in die Standardausgabe aus
- `cat`: Ausgabe von Dateien
	- `cat` kann mit speziellen Eingaben arbeiten
	- `?`: Platzhalter für einen beliebiges Zeichen
	- `*`: Platzhalter für beliebige Zeichen, kann auch keine Zeichen akzeptieren

# Eingabeumleitung
---
- Eingabeumleitung werden zwischen Befehlen verwendet: `>, >>, <`
	- `>>`: Fügt die Ausgabe einer Datei hinzu
	- `>`: Schreibt/Überschreibt eine Datei mit einer Ausgabe
	- `<`: Standardeingabe wird mit einer Datei gefüllt
		- Bsp. `cat` ohne Argumente aufruft, dann öffnet sich die Standardeingabe
		- Diese kann mit `<` umgeleitet werden
- Pipeline: `|`
	- Leitet die Ausgabe eines Befehls zu der Eingabe des nächsten Befehls um
	- Bsp: `cat test.txt | wc -l` <=> `wc -l test.txt`

# Dateien
---
- Standardeingabe `stdin`: Eine Zwischenablage für Eingabe von Außen
- Standardausgabe `stdout`: Ein Zwischenablage wo Ausgaben jeglicher Art landen
# Dateinamen
---
- Linux: Achtet auf Groß- und Kleinschreibung
- Mac/Windows: Achtet NICHT auf Groß- und Kleinschreibung

# Dateimanipulation
---
- `mv`: Verschiebt eine Datei in einen neuen Zielbereich
	- `mv source target`
	- Bsp.: `mv hello.txt wd25_tz_d01`
		- `wd25_tz_d01` ist ein Ordner, der Dateiname wird beibehalten
	- Kann verwendet werden um eine Datei umzubenennen
- `touch`: Erstellt eine Datei
- `cp`: Kopiert Dateien und den Inhalt in eine neue Datei
- `rm`: Löscht Dateien und Dateiverzeichnisse
	- Das Löschen einer Datei oder eines Ordners ist unwiderruflich
	- Ordner löschen mit: `rm -r` 
- `mv, cp, rm`
	- Diese Befehle verwendet das Zeichensystem, ähnlich wie bei `cat`
	- `?`: Platzhalter für einen beliebiges Zeichen
	- `*`: Platzhalter für beliebige Zeichen, kann auch keine Zeichen akzeptieren
```
Test ----
		|
		test-copy.txt
		tmp -----
				|
				hello.txt
```

- `wc`: Zählt einige Eigenschaften von Dateien
	- `wc -l <datei>`: zählt die Anzahl an Zeilen in einer Datei
	- `wc -c <datei>`: zählt die Anzahl an Bytes in einer Datei
	- `wc -m <datei>`: zählt die Anzahl an Zeichen in einer Datei
	- `wc -w <datei>`: zählt die Anzahl an Wörter in einer Datei
	- wird keine Datei angegeben, dann ließt `wc` die Eingabe aus der Standardeingabe (`stdin`)

## Aufgabe: Text am Anfang anfügen

```bash
# Mettel
echo "New Line" > test_2.txt
cat test_2.txt test.txt > test_3.txt
cat test_3.txt
mv test_3.txt test.txt
```

```bash
# Willbrand
echo "New Line" > tmp.txt
cat test.txt >> tmp.txt
mv tmp.txt test.txt
```

```bash
# Eschke
echo "New Line" | cat - test.txt > temp && mv temp test.txt
```
