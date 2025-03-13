# Mehr Befehle

## wc - Word Count

- `wc -l <datei>`: zählt die Anzahl an Zeilen in einer Datei
- `wc -c <datei>`: zählt die Anzahl an Bytes in einer Datei
- `wc -m <datei>`: zählt die Anzahl an Zeichen in einer Datei
- `wc -w <datei>`: zählt die Anzahl an Wörter in einer Datei
- wird keine Datei angegeben, dann ließt `wc` die Eingabe aus der Standardeingabe (`stdin`)

## uniq

- unique = einzigartig
- Standardeingabe oder mit einer Datei als Argument

## man

- Gibt eine Beschreibung eines Linux Befehls aus

## sort

- Sortiert standardmäßig Zeichenketten, also jede Zahl und jeder Buchstabe wird als Zeichen angesehen und die Rangordnung der Zeichen wird übernommen
  - 0-9 < A-Z < a-z
  - Um numerisch zu sortiert gibt es die `-n` Option
    - Jedes Zeichen wird mit der Rangordnung 0 angesehen, aber die Reihenfolge der Buchstaben bleibt erhalten
  - `sort` kann auch nach bestimmten Spalten sortieren, wenn die Eigabe ein bestimmtes Format besitzt: z.B. `Sono,184`
