### Laboratorium 4

1\. Wyświetl listę plików z aktualnego katalogu, zamieniając wszystkie małe litery na duże.
```bash
ls -l | tr '[a-z]' '[A-Z]'
```

2\.Wyświetl listę praw dostępu do plików w aktualnym katalogu, ich rozmiar i nazwę.
```bash
ls -l | awk '{print $1,$5$8}'
```

3\. Wyświetl listę plików w aktualnym katalogu, posortowaną według rozmiaru pliku.
```bash
ls -l -S
ls --sort=size -l
```

4\. Wyświetl zawartość pliku /etc/passwd posortowaną według numerów UID w kolejności od największego do najmniejszego.
```bash
sort -t : -n -k3 -r /etc/passwd
```

5\.Wyświetl zawartość pliku /etc/passwd posortowaną najpierw według numerów GID w kolejności od największego do najmniejszego, a następnie UID
```bash
sort -t : -k4 -r /etc/passwd | sort -t : -k3
```

6\.Podaj liczbę plików każdego użytkownika.
```bash

```

7\. Sporządź statystykę praw dostępu (dla każdego z praw dostępu podaj ile razy zostało ono przydzielone
```bash
find -printf "%m\n" | sort | uniq -c
3 razy ?
```

8\.Czy potrafisz odpowiedzieć jaki będzie efekt wykonania poniższych poleceń?
```bash
ls -l > lsout.txt                           #  1  Wypisuje liste plików 
ls -la >> lsout.txt                         #  2  Dopisuje liste plikow oraz tych ukrytych 
ps >> psout.txt                             #  3  Do pliku dopisuje liste uruchomionych procesów
free -m >> ~/wynik                          #  4  Dopisuje wolną ilość pamieci
kill -1 1234 > killout.txt 2>killerr.txt    #  5  zabij proces o id 1234 i zapisz to w pliku killerr.txt ...
kill -1 1234 > killout.txt 2>&1             #  6  
kill -1 1234 > /dev/null 2>&1               #  7
sort psout.txt > pssort.txt                 #  8  posortuj liste plikow z psout.txt i wpisz do pssort.txt
ps | sort > pssort.txt                      #  9  posortuje liste procesow i wpisze do pssort.txt
cat lsout.txt | sort > lssort.txt           # 10  posortuje liste plikow z lsout.txt i wpisze do lssort.txt
who | sort | more                           # 11  posortuje liczbe zalogowanych 
who | sort | less                           # 12  
find -type f | wc                           # 13
find -type f -print0 | wc --files0-from=-   # 14
```
