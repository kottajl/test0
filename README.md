<h1>Aplikacja do hotelowego systemu rezerwacji</h1>

## Skład grupy _Awokado_
**Patryk Czuchnowski** (patczuch@student.agh.edu.pl) <br />
**Michał Pędrak** (michalpedrak@student.agh.edu.pl) <br />
**Andrzej Wacławik** (wajarema@student.agh.edu.pl) <br />

## Charakterystyka problemu
W ramach projektu tworzymy aplikację do zarządzania rezerwacjami pokoi dla pracowników pewnej firmy hotelowej.
Pracownik powinien mieć możliwość:
- wyszukania dostępnego pokoju w wybranym terminie (także z wybranymi kryteriami, np. z daną liczbą łóżek)
- dokonania rezerwacji wybranego pokoju dla danego klienta w wybranym terminie
- anulowania wybranej rezerwacji

## Budowane rozwiązanie problemu
Nasza aplikacja budowana jest w języku Java, przy wykorzystaniu framework'a Spring Boot.
Dodatkowo wykorzystujemy Hibernate do utworzenia prostej bazy danych oraz JavaFX do projektowania widoku naszej aplikacji.

<h3>Baza danych:</h3>
Dane zasadniczo przechowywane są w dwóch tabelach reprezentowanych przez klasy ***Room*** i ***Reservation***:


- _**Room**_ — tabela z informacjami o pokojach hotelowych, posiadająca pola:
  - _**roomID**_ - unikalne ID pokoju
  - _**roomNumber**_ - numer pokoju
  - _**floorNumber**_ - numer piętra, na którym znajduje się pokój
  - _**numberOfSingleBeds**_ - liczba pojedynczych łóżek znajdujących się w pokoju
  - _**numberOfDoubleBeds**_ - liczba podwójnych (małżeńskich) łóżek znajdujących się w pokoju
  - _**pricePerDay**_ - cena pokoju za jedną dobę hotelową
  - _**TVpresent**_ - czy pokój posiada telewizor
  - _**balconyPresent**_ - czy pokój posiada balkon
  - _**directionOfWindow**_ - na którą stronę jest widok z okien pokoju


- _**Reservation**_ - tabela z informacjami o rezerwacjach, posiadająca pola:
  - _**reservationID**_ - unikalne ID rezerwacji
  - _**customer**_ - informacje o kliencie dokonującym rezerwacji:
    - _**firstName**_ - imię klienta
    - _**lastName**_ - nazwisko klienta
    - _**phoneNumber**_ - numer telefonu klienta
  - _**room**_ - rezerwowany pokój
  - _**startDate**_ - data początku rezerwacji
  - _**finishDate**_ - data końca rezerwacji


<h3>Diagram klas UML</h3>

<img src="img/uml_diagram.png">
