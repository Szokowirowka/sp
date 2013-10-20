## Rozwiązania zadan z basha 1

1\. Używając linii poleceń stwórz strukturę katalogów:


```sh
mkdir dom -p nauka/{c,logo,pascal} praca/{dokumenty,zlecenia/{niezrealizowane,zrealizowane}} ...
```

2\. Przejdź do katalogu dom i utwórz katalog wazne-sprawy.

```sh
cd dom 
mkdir wazne-sprawy

```
3\. Wejdź do katalogu wazne-sprawy i utwórz tam pusty plik rachunki.txt.

```sh
cd dom/wazne-sprawy
touch rachunki.txt
```
4\. Będąc w katalogu wazne-sprawy skopiuj plik rachunki.txt do katalogu zrealizowane.

```sh
cp rachunki.txt ../../praca/zlecenia/zrealizowane
```

5\. Przejdź do katalogu zrealizowane i zmień nazwę pliku rachunki.txt na wykonano.txt

```sh
mv rachunki.txt wykonano.txt
```

6\.Utwórz plik wykonano.txt wielkości 11 bajtów, następnie podziel go pliki wielkości 5 bajtów. W ten sposób otrzymasz 3 pliki

```
echo 1234567890 > wykonano.txt
split --bytes=5 wykonano.txt
```

7\. Będąc w katalogu logo skopiuj powyżej otrzymane 3 pliki do katalogu dokumenty

```
cd srodowisko/tmp/temp/nauka/logo
cp ../../praca/zlecenia/zrealizowane/x* ../../praca/dokumenty
```
8\.Będąc w katalogu dokumenty połącz skopiowane 3 pliki w plik odtworzono.txt, tak aby otrzymać plik o zawartości identycznej z wykonano.txt. Następnie plik odtworzono.txt skopiuj do katalogu wazne-sprawy

```
cat x* > odtworzono.txt
cp odtworzono.txt ../../dom/wazne-sprawy
```

9\. Będąc w katalogu wazne-sprawy sprawdź, czy są jakieś różnice w zawartości plików wykonano.txt i odtworzono.txt

```
diff ./wykonano.txt ../../praca/zlecenia/zrealizowane/odtworzono.txt
```
