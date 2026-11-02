# Wynik kontrolny: agent zapytań ofertowych

Liczby poniżej policzono niezależnie z plików w katalogu `dane-cwiczeniowe/`. Jeśli agent oddaje inne wartości, procedura nie działa poprawnie w Waszym narzędziu.

## Sprawdź wynik na danych kontrolnych

Porównaj odpowiedź z tabelami poniżej. Liczby policzyliśmy niezależnie z tych samych plików.

| Projekt | Masa | Marża ofertowa | Marża powykonawcza | Zwłoka płatności | Zmiany zakresu |
|---|---|---|---|---|---|
| P-2025-001 | 34,0 t | 15,0% | 6,7% | 12 dni | 2 |
| P-2024-004 | 41,0 t | 15,0% | 6,5% | 35 dni | 3 |
| P-2025-009 | 29,5 t | 15,1% | 12,8% | 0 dni | 0 |

| Gniazdo | Norma | Potrzeba na 36 t | Wolne moce | Okno |
|---|---|---|---|---|
| Spawanie | 22,6 rbh/t | 813 rbh | 222 rbh | tygodnie 18–27, przed montażem |
| Montaż | 15,2 rbh/t | 548 rbh | 262 rbh | tygodnie 28–31, termin klienta |

Prawidłowa ocena to **„wyceniać pod warunkami”**: dwa z trzech podobnych tematów straciły ponad połowę marży na zmianach zakresu i opóźnieniach, a w terminie klienta zakładowi brakuje mocy zarówno na spawalni, jak i na montażu. Warunki do rozmowy: późniejszy termin montażu albo kooperacja, aneks wyceniający zmiany po zamrożeniu listy materiałowej, zaliczka zamiast płatności 60 dni po odbiorze przy karze 0,5% za dzień zwłoki. W brakach agent powinien wskazać rysunki wykonawcze (tylko koncepcja) i nieznany termin gotowości fundamentów.

Jeśli w tabeli podobnych projektów pojawi się hala albo wiata bez montażu, agent nie trzymał się reguły. Jeśli liczby mocy się nie zgadzają, sprawdź, czy rzeczywiście liczył kodem.

## Krok z rzeczywistością

Dane w firmie się zmieniają, a agent musi to zauważyć bez zmiany instrukcji. Otwórz `projekty-zamkniete.xlsx`, dopisz na końcu jeden wiersz i podmień plik w wiedzy projektu:

```text
P-2026-025 | 2026 | Ferma Kurzanka sp. z o.o. | wiata magazynowa | S355 | 40 | ocynk ogniowy | tak | 700000 | 595000 | 690000 | 160 | 1000 | 680 | 60 | 0 | 1 | Niedoszacowane spawanie słupów.
```

Zadaj w nowej rozmowie to samo pytanie. Agent powinien teraz pokazać **cztery** podobne projekty, z nowym na drugim miejscu (różnica masy 4 t). Norma spawania wzrośnie do 23,3 rbh/t, czyli 837 rbh na 36 t; norma montażu do 15,7 rbh/t, czyli 566 rbh. Nowy projekt ma marżę ofertową 15,0% i powykonawczą 1,4%.

Jeden zły projekt przesunął normę i obraz marży. Właśnie dlatego koszt zamkniętego zlecenia ma wracać do wiedzy agenta, a nie do szuflady.
