### Podstawowe komendy
* `pwd` – print working directory
* `ls` – listowanie zawartości | parameter -l pokazuje uprawnienia | parametr -a pokazuje ukryte (.) |
* `mkdir` – make directory (tworzy katalog)
* `touch` ‘nazwa pliku’ – tworzy plik
* `head` – wyświetlenie początku pliku
* `tail` – wyświetlenie od końca || parametry [-liczba linii do wyświetlenia] [ścieżka]
* `sort` [-opcje] [ścieżka]
* `nl` – numer line (ponumeruje linijki)
* `read` – wprowadzanie danych przez uzytkownika

### Wildcards – znaki specjalne
* `*` – dowolna ilość, dowolne znaki
* `?` – jeden dowolny znak
* `[ ]` – umieszczony wewnątrz zakres znaków
* `^` – znak negacji (tak jak w cpp !)

### Wyrażenia regularne
* `.` – pojedynczy znak
* `?` – poprzedni znak pojawia się 0 lub 1 raz
* `*` – poprzedni znak pojawia się 0 lub więcej razy
* `+` – poprzedni znak pojawia się 1 lub więcej razy
* `{n}` – poprzedni znak pojawia się n lub więcej razy
* `{n,m}` – poprzedni znak pojawia się od n do m razy
* `[abc]` – znak jest jednym z wymienionych w nawiasie
* `[^abc]` – znak NIE jest jednym z wymienionych w nawiasie
* `()` – pozwala na grupowanie znaków
* `|` – operacja logiczna OR (lub)
* `^` – początek linii
* `$` – koniec linii (znak LF)

### SHORTHANDS
* `\w` – określa znaki słów, czyli z zakresu [A-Z a-z 0-9]
* `\s` – określa białe znaki (spacja itp.)
* `--` nie wspierane
* `\d` – określa cyfry 0-9

### Piping & Redirection
* `>` - zapis wyjścia do pliku
* `>>` - dopisanie wyjścia do istniejącego pliku
* `|` - przekierowanie wyjścia do innego polecenia/programu
* `<` - wczytanie pliku na input
* `2>` - zapis błędów z wyjścia do pliku

### Bash | C
* `-eq ==`
* `-gt >`
* `-lt <`
* `-ge >=`
* `-le <=`

### Porównywanie STRINGów
Bash | C
* = == (równa się)
* != != (nie równa się)

### Operacje matematyczne
```sh
zm1=2
zm2=4
wynik=$(($zm1+$zm2))
echo $wynik
```

### Backticks
Backticks ` `` ` (znaki nad tyldą - ~) umożliwia zamknięcie wyniku polecenia do zmiennej

Np. wynik=`grep ^[Aa] jajco.txt | wc -l` zamknie wynik polecenia do zmiennej wynik

### Argumenty w skryptach
* `$0` – nazwa skryptu
* `$1-9` – argumenty z linii poleceń
* `$#` - ilość argumentów podanych w terminalu

### Instrukcja warunkowa – przykład składni
```sh
if [ warunek ]; then
  robi_to
elif [ warunek ]; then
  robi to
else
  robi to
fi
```

### Pętla while – składnia
```sh
while [ warunek ]
do
  wykonaj
done
```

### Pętla until – wykonuje dopóki warunek nie jest spełniony
```sh
untill [ $zmienna -le 0 ]
do
  echo obejście pętli numer: $zmienna
  ((zmienna--))
done
```


### Pętla for – pętla wykonuje się tyle razy ile argumentów jej podamy
```sh
Zmienna=’arg1 arg2 arg3’
for <var> in $zmienna
do
  wykonaj
done
```
