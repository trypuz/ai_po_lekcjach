# AI po lekcjach

## Organizacja tekstu w notatnikach

Notatniki powinny być zorganizowane zgodnie z zasadami podanymi poniżej. 

Celem "sztywnej" organizacji zawartości notatników jest późniejsza możliwość automaczycznego wygenerowania slajdów prezentacji LaTeX/Beamer.

Notatnik należy traktować jako rozdział większej całości.

### Nagłówki

Pierwsze trzy poziomy nagłówków powinny być używane w następujący sposób.

- Nagłówek pierwszego poziomu,'#', występuje tylko na początku w pierwszej komórce. To **tytuł rozdziału**. Pierwsza komórka nie powinna zawierać niczego innego poza nagłówkiem pierwszego poziomu.
- Nagłówek drugiego poziomu,'##', odpowiada **tytułowi sekcji rozdziału**. Powinien znajdować się w osobnej komórce.
- Nagłówek trzeciego poziomu, '###', odpowiada **paragrafowi sekcji**. Będzie również odpowidał **tytułowi slajdu**. Nagłówek trzeciego poziomu, wraz z treścią paragrafu powinien znajdować się w jednej komórce.

Pisząc "myśl slajdami"!

### Bibliografia

- Sekcja "Bibliografia" jest obowiązkowa i powinna znaleźć się na końcu.
- Musi być sformatowana jak poniżej:

```
## <span t="slide_title">Bibliografia</span>
- <span t="l1">Pierwsza pozycja</span>
- [<span t="l1">URL do materiałów</span>](URL do materiałów)
```
### Obrazy

Obrazy należy umieszczać za pomocą HTMLowego
```
<img src="../KATALOG/NAZWA_PLIKU" width="XXX">
```

`KATALOG` może mieć trzy wartości:

- `pliki_yEd` - to katalog zawierający obrazy utworzonych za pomocą yEd i ich źródła; obrazy utworzone za pomocą yEd powinny zostać wyeksportowane do formatu PNG.
- `pliki_z_internetu` - to katalog obrazów pobranych z internetu; w folderze znajduje się plik zrodla_zdjec.md, gdzie należy podać skąd został pobrany obraz
- `pliki_wlasne` - to katalog obrazów własnych innych niż obrazy utworzonych za pomocą yEd

### Treść slajdów

Napisaliśmy wyżej, że nagłówek trzeciego poziomu, '###', odpowiada paragrafowi sekcji i tytułowi slajdu jednocześnie, i że nagłówek trzeciego poziomu, wraz z treścią paragrafu powinien znajdować się w jednej komórce. 

Treść paragrafu, którą chcemy umieścić na slajdzie należy otoczyć znacznikami `<span t="TAG"></span>`. Wartościami `TAG` mogą być:

- `l1` - element listy poziomu 1
- `l2` - element listy poziomu 2
-  `q` - cytat lub definicja
-  `v` - kod, który zostanie umieszczony w środowisku verbatim

Jeśli w kolejnej komórce nie będzie tytułu (czyli nagłówka poziomu trzeciego), to slajd koresponsujący z tą komórką  będzie miał ten sam tytuł co poprzedni.

Umieść tabelę markdowna w znacznikach: `<div t="t"> TABELA_MARKDOWN </div>`, jeśli chesz, aby znalazła się na slajdach

## Generowanie slajdów

Aby wygenerować slajdy skorzystać z notatnika ipynb2beamer.ipynb. Skrypt generuje slajdy dla wszystkich notatników ze wskazanych folderów.

Wygenerowane slajdy znajdują się w pliku z rozszerzeniem `.tex` w katalogu `beamer`.

