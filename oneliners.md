#### wyświetla tylko podaną kolumne rozdzielone spacjami
```sh
cut -f 4 -d ' ' data.txt
```
#### to samo dla tabulatora
```sh
cut -f 2 -d $'\t' data.txt
```

#### stream editor zamienia tabulatory na spacje, gdzie `g` to wszystkie wystąpienia w lini, a `s` to switch `s/co_zamieniam/na_co_zamieniam/g`
```sh
sed 's/\t/ /g' data.txt
```
#### tu zamienia taby na spacje i wycina do pokazania tylko 2 i 6 kolumne - rozdzielone spacjami
```sh
sed 's/\t/ /g' data.txt | cut -f 2,6 -d ' '
``` 
#### uniq wyświetla unikalne linie tylko jeżeli sa posortowane - dlatego zawsze sort
```sh
cat text.txt | sort | uniq
```
#### krótsza wersja tego 
```sh
sort -u text.txt
```

## wyswietlanie zawatrosci danego pliku
* `cat` - wyświetla caly plik odrazu
```sh
cat text.txt
```
* `less` - wyświetla plik umożliwiając płynne przewijanie linikjka po linijce oraz umożliwia przeszukiwanie
używając '/szukana_fraza', n(następny wynik) oraz N(poprzedni wynik) umożliwiają przechodzenie pomiędzy szukanymi frazami płynnie
```sh
less text.txt
```
* `more` - wyświetla plik strona po stronie
```sh
more text.txt
```
