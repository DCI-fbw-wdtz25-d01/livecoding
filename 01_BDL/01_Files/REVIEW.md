# Review

## Dateien

```bash
mkdir test
cd test
echo "Test" > test1.txt # Z1
echo "Test" > test2.txt # Z1
echo "Test" > test10.txt # Z1
cat test1.txt test2.txt >> output.txt # Z2
cat test*.txt >> output.txt # Z5
cat test?.txt >> output.txt # Z7
rm test*.txt # mehrere Dateien löschen
mv output.txt .. # Datei wird in den Elternordner verschoben
cp ../output.txt result.txt # Inhalt der Datei wird kopiert
wc -l ../output.txt
```

