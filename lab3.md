### Laboratorium 3

1\. Wyświetl plik /etc/passwd z podziałem na strony przyjmując, że strona na 5 linii tekstu. (raczej more niż less)
```bash
cat /etc/passwd | more -5
```
2\. Korzystając z polecenia cat utwórz plik tekst3.txt, który będzie składał się z zawartości pliku tekst1.txt, ciągu znaków podanego ze standardowego wejścia (klawiatury) i pliku tekst2.txt.
```bash
cat > tekst1.txt      1165465465211616
cat > tekst2.txt      9879787897979879879
cat tekst1.txt > tekst3.txt          
cat >> tekst3.txt             ala ma kota
cat tekst2.txt >> tekst3.txt
cat tekst3.txt
```

3\.Wyświetl po 5 pierwszych linii wszystkich plików w swoim katalogu domowym w taki sposób, aby nie były wyświetlane ich nazwy
```bash
head -qn 5 *
```

4\. Wyświetl linie o numerach 3, 4 i 5 z pliku /etc/passwd
```bash
head -n 5 /etc/passwd | tail -n 3
```

5\.Wyświetl linie o numerach 7, 6 i 5 od końca pliku /etc/passwd
```bash
tail -n 7 /etc/passwd | head -n 3
```

6\.Wyświetl zawartość pliku /etc/passwd w jednej linii
```bash
