# Task 1 
## Subtask 1 
10 punktów 
## Subtask 3 
Cześć! Jestem Dorota i nie lubię stać w miejscu. Lubię za to ciągle się rozwijać i uczyć nowych umiejętności. Jestem zdania, że każdy człowiek może nas czegoś nauczyć. Liczę więc tutaj na solidną dawkę wiedzy.
## Subtask 4
1. Aplikacja jest to panel zarządzania graczami, meczami i do tworzenia raportów.
2. 
* Po wejściu na stronę aplikacji widnieje panel logowania: loginem i hasłem. Login = email - co może być mylące dla użytkownika. Hasło pojawia się od razu jako zakodowany ciąg znaków i nie można go podejrzeć po wpisaniu. Istnieje możliwość przypomnienia hasła, które trafia na naszego maila. Nie ma możliwości rejestracji nowego użytkownika dla tej aplikacji.
* Po zalogowaniu się aplikacja przenosi nas na stronę główną. Użytkownik może na niej sprawdzić listę graczy, dodać nowego gracza lub edytować istniejącego, stworzyć raport dla gracza, opis meczu, w którym zagrał, listę jego aktywności meczowych a także edytować te informacje. 
* Strona dostępna jest w angielskiej wersji językowej.
Layout dla aplikacji stworzony jest w sposób chaotyczny i nieintuicyjny. Kontakt do Dev teamu mógłby znajdować się na dole strony w tak zwanej stopce. Niektóre przyciski (button) w polskiej wersji językowej nie zostały przetłumaczone na język polski. O ile div z ilością graczy jest zasadny, to pozostałe trzy (ilość meczy, raportów, akcji) nie wnoszą żadnej wartości dla użytkowników panelu. Aplikacja prawdopodobnie przeznaczona jest dla ściśle wyselekcjonowanych pracowników firmy skautingowej, ponieważ pola tekstowe w zasadzie nie posiadają walidacji, więc user posiadający dostęp musi dbać o poprawność i jakość dodawanych przez siebie danych.
3. Pomysł aplikacji dla firmy skautingowej jest wartościowy. Apka jest prosta, ale jej interfejs pozostawia wiele do życzenia. Prawdopodobnie w teamie zabrakło ui designera, a szkoda.
4. Strona choć prosta, zecydowanie nieintuicyjna. Podzakładki mecze i raporty zawierają te same informacje, które mogłyby być skumulowane w jednej zakładce. W aplikacji zastosowano wiele ciekawych rozwiązań i ułatwień, nistety ich implementacja wymaga jeszcze dopracowania.
5.
### * Link do kontaktu z teamem dev nie działa.

Srodowisko: Google Chrome Wersja 112.0.5615.138

Kroki do reprodukcji:
1. Zalogowany użytkownik znajduje się na stronie głównej aplikacji.
2. Użytkownik klika w aktywny link "DEV team contact"

Oczekiwany rezultat:
Użytkownik zostaje przeniesiony na stronę z kontaktem do teamu developerskiego.

Rzeczywisty rezultat:
Użytkownik zostaje przeniesiony na stronę do logowania do aplikacji Slack.

Załącznik numer 1





### * Brak walidacji dla pola: "data urodzenia" w zakładce dodawanie nowego gracza

Srodowisko: Google Chrome Wersja 112.0.5615.138

Kroki do reprodukcji:
1. Zalogowany użytkownik znajduje się na stronie głównej aplikacji.
2. Użytkownik klika w aktywny link "dodaj nowego gracza"
3. Użytkownik ustawia datę urodzenia gracza na dziś. Na przykład 24.04.2023

Oczekiwany rezultat:
Aplikacja powiadamia użytkownika, że niemożliwe jest dodanie gracza młodszego niż 12, 13 lat?(To zależy od dokumentacji projektowej)

Rzeczywisty rezultat:
Błędna data urodzenia zostaje zachowana. Możliwe jest także zachowanie daty z przyszłości. Na przykład: 2035 rok.

Załącznik numer 2





### * Przyciski w aplikacji są w róznych językach

Srodowisko: Google Chrome Wersja 112.0.5615.138

Kroki do reprodukcji:
1. Zalogowany użytkownik znajduje się na stronie głównej aplikacji.
2. Użytkownik klika w aktywny link "dodaj nowego gracza"
3. Przed użytkownikiem pojawia się formularz tekstowy do wypełnienia

Oczekiwany rezultat:
Wszystkie nazwy pól tekstowych oraz nazwy przycisków w polskiej wersji językowej są po polsku.

Rzeczywisty rezultat:
Nazwy niektórych przycisków(buttonów) są po angielsku

Załącznik numer 3





### * Pole tekstowe telefon przyjmuje litery, znaki specjalne oraz zbyt długi ciąg znaków

Srodowisko: Google Chrome Wersja 112.0.5615.138

Kroki do reprodukcji:
1. Zalogowany użytkownik znajduje się na stronie głównej aplikacji.
2. Użytkownik klika w aktywny link "dodaj nowego gracza"
3. Przed użytkownikiem pojawia się formularz tekstowy do wypełnienia
4. W polu tesktowym telefon użytkownik wpisuje lol&&&&&

Oczekiwany rezultat:
Aplikacja wysyła komunikat o niepoprawnym formacie/Ilości znaków

Rzeczywisty rezultat
Użytkownik w polu telefon może wpisać cokolwiek.

Załącznik numer 4





### * Pola tekstowe waga i wzrost przyjmują ujemne wartości

Srodowisko: Google Chrome Wersja 112.0.5615.138

Kroki do reprodukcji:
1. Zalogowany użytkownik znajduje się na stronie głównej aplikacji.
2. Użytkownik klika w aktywny link "dodaj nowego gracza"
3. Przed użytkownikiem pojawia się formularz tekstowy do wypełnienia
4. W polu tesktowym waga/wzrost użytkownik wpisuje wartość ujemną -41

Oczekiwany rezultat: 
Użytkownik otrzymuje komunikat o niepawidłowym formacie dla pól tekstowych.

Rzeczywisty rezultat:
Możliwe jest dodanie ujemnej wagi i wzrostu

Załącznik numer 5





### * Strona nieresponsywna dla zakładek mecze i raporty

Srodowisko: Google Chrome Wersja 112.0.5615.138

Kroki do reprodukcji:
1. Zalogowany użytkownik znajduje się na stronie głównej aplikacji.
2. W menu głównym użytkownik wybiera zakładkę "gracze" oraz gracze na przykład: Brzęczyszcykiewić
3. W menu głównym użytkownik wybiera zakładkę mece/raporty

Oczekiwany rezultat:
Strona dopasowuje się do urządzenia

Rzeczywisty reultat:
Strona nie jest dopasowana do urządzenia

Załącznik numer 6





### * Parametry start i limit są przestarzałe

Srodowisko: Google Chrome Wersja 112.0.5615.138

Kroki do reprodukcji:
1. Zalogowany użytkownik znajduje się na stronie głównej aplikacji
2. w narzędziach developerskich użytkownich przechodzi do konsoli
3. Użytkownik klika w zakładkę gracze

Oczekiwany rezultat:
W konsoli nie pojawiają się błedy i ostrzeżenia

Rzeczywisty reultat:
W konsoli pojawiają się błedy i ostrzeżenia

Załącznik numer 7





### * Nie działa przycisk clear przy edycji istniejacego gracza

Srodowisko: Google Chrome Wersja 112.0.5615.138

Kroki do reprodukcji:
1. Zalogowany użytkownik znajduje się na stronie głównej aplikacji.
2. W menu głównym użytkownik wybiera zakładkę "gracze" na przykład: Brzęczyszcykiewić
3. Użytkownik klika w przycisk clear aby wyczyścić wszytskie pola w edycji gracza

Oczekiwany rezultat:
Wszystkie pola w edycji są puste

Rzezywisty rezultat:
Formularz edycji nie zostaje wyczyszczony

Załacznik numer 8




https://drive.google.com/drive/folders/1NhnSf70UaKHvdV6QoUy05Vro1hLqtCGx?hl=pl


# Task 2

## Subtask 3
Głównym celem przypadku testowego jest upewnienie się, czy różne funkcje aplikacji działają zgodnie z oczekiwaniami. Pomaga testerowi zweryfikować, czy aplikacja jest wolna od wad i czy działa zgodnie z oczekiwaniami użytkowników końcowych. Do innych zalet zaliczamy:
*  Zapewnienie dobrego pokrycia testowego;
*  Pomoc w poprawie jakości oprogramowania;
*  mniejsze koszty utrzymania i wsparcia oprogramowania;
*  weryfikacja czy oprogramowanie spełnia wymagania użytkownika końcowego.

https://drive.google.com/drive/folders/1-sOL111i5sx5EtUlRIDS5QPiUxwFOZSF?hl=pl

### Zadanie dodatkowe w jira;)


# Task 3

## Subtask 2

https://drive.google.com/drive/folders/13NzlGnFR22o9mXPfMFG0n3q857smRcv3?hl=pl

## Subtask 3

https://drive.google.com/drive/folders/13LqbglRkXrvUIlx-3EaA9jkpzBBPgEAC?hl=pl


# Task 4

## Subtask 2

https://drive.google.com/drive/folders/1cuqwU0VZyCAZuguwERE1Qty3iIzUS0W_?hl=pl

## Subtask 3

* OLX jest serwisem ogłoszeniowym służącym do sprzedawania oraz kupowania towarów i usług. 
* Użytkownikiem aplikacji jest sprzedający towar i usługi (osoba prywatna lub firma) oraz kupujący, którym także może być osoba prywatna lub firma.
* Aplikacja jest przyjazna dla użytkownika. Interfejs jest czytelny i przejrzysty. Towary i usługi podzielone są na kategorie. W serwis wbudowana została także wyszukiwarka, która usprawnia przeszukiwanie tak wielu ogłoszeń. Za zakupy można zapłacić płatnościami online, a towar zamówić pocztą polską, kurierem, paczką do paczkomatu lub odebrać osobiście. Twórcy serwisu nieustannie pracują nad bezpieczeństwem zakupów swoich uzytkowników. Serwis więc stale się rozwija.
* W aplikacji należy popracować nad filtrowaniem. Aktualnie filtrujemy po: najdroższym, najtańszym, najnowszym oraz tak zwany "wybór la Ciebie". Zabrakło tak podstawowego filtrowania jak po rzeczy nowe i używane.
* W aplikacjach mobilnych, natywnych największą rolę odgrywa responsywność. Strona powinna być dostosowana do urzadzenia, na którym będzie wyśiwetlana, a mnogość takich urządzeń w tych czasach jest naprawdę duża. Osoba testująca kontroluje jakość wyświetlania treści, obrazów, linków oraz innych mediów. Czytelność względem rozmiarów ekranu, skrolowanie, padding, zmiany kolorów i podświetleń. Wyświetlana treść powinna być czytelna oraz a klikalne obszary posiadać odpowiedni rozmiar. 


# Task 5

## Subtask 3

* Wyświetl tabelę actors w kolejności alfabetycznej sortując po kolumnie surname.

![sql_1](https://github.com/DorotaKw/test_portfolio/assets/69016457/76f22d8b-7f97-411b-a49d-51610963265f)

* Wyświetl film, który powstał w 2019 roku.

![sql_2](https://github.com/DorotaKw/test_portfolio/assets/69016457/356c730d-a234-40cc-a5fc-4485c8f87713)

* Wyświetl wszystkie filmy, które powstały między 1900, a 1999 rokiem.

![sql_3](https://github.com/DorotaKw/test_portfolio/assets/69016457/3b33b85c-5063-4a36-93ac-5100a11439e3)

* Wyświetl JEDYNIE tytuł i cenę filmów, które kosztują poniżej 7$

![sql_4](https://github.com/DorotaKw/test_portfolio/assets/69016457/f7640c5e-0606-4439-8402-1bc58bf84ae6)

* Użyj operatora logicznego AND, aby wyświetlić aktorów o actor_id pomiędzy 4-7 (4 i 7 powinny się wyświetlać). NIE UŻYWAJ operatora BETWEEN.

![sql_5](https://github.com/DorotaKw/test_portfolio/assets/69016457/d46ba5da-2ec4-4ad7-b59f-503f59401b56)

* Wyświetl klientów o id 2,4,6 wykorzystaj do tego warunek logiczny.

![sql_6](https://github.com/DorotaKw/test_portfolio/assets/69016457/1e9833a2-8324-4116-8452-f58bbee86727)

*  Wyświetl klientów o id 1,3,5 wykorzystaj do tego operator IN.

![sql_7](https://github.com/DorotaKw/test_portfolio/assets/69016457/8f37fa1e-da5a-4687-aaeb-3e9cabc13405)

* Wyświetl dane wszystkich osób z tabeli ‘actors’, których imię zaczyna się od ciągu “An”.

![sql_8](https://github.com/DorotaKw/test_portfolio/assets/69016457/8655b53d-b250-4d0a-8f2d-c12ff9f8a656)

* Wyświetl dane klienta, który nie ma podanego adresu email.

![sql_9](https://github.com/DorotaKw/test_portfolio/assets/69016457/4d1fb53c-dc8c-47e9-ab5e-4e110bf4311a)

* Wyświetl wszystkie filmy, których cena wynosi powyżej 9$ oraz ich ID mieści się pomiędzy 2 i 8.

![sql_10](https://github.com/DorotaKw/test_portfolio/assets/69016457/2ae555b8-42a9-4b5f-880f-0c45e4446c0b)

## Task 6

* Popełniłam błąd wpisując nazwisko Ani Miler – wpisałam Muler. Znajdź i zastosuj funkcję, która poprawi mój karkołomny błąd 🙈

UPDATE customers
SET surname = 'Miler'
WHERE customer_id = 3

![sql_11](https://github.com/DorotaKw/test_portfolio/assets/69016457/c2660f80-bfe6-45ba-a2bd-56755ced3ec3)

* Pobrałam za dużo pieniędzy od klienta, który kupił w ostatnim czasie film o id 4. Korzystając z funkcji join sprawdź, jak ma na imię klient i jakiego ma maila. W celu napisania mu wiadomości o pomyłce fantastycznej szefowej

SELECT name, email FROM sale JOIN customers ON customers.customer_id=sale.customer_id WHERE movie_id=4;

![sql_12](https://github.com/DorotaKw/test_portfolio/assets/69016457/bb3fe68d-0eec-4958-8aa1-4804a688b780)

* Na pewno zauważyłaś, że sprzedawca zapomniał wpisać emaila klientce Patrycji. Uzupełnij ten brak wpisując: pati@mail.com

UPDATE customers
SET email='pati@mail.com'
WHERE name='Patrycja'

![sql_13](https://github.com/DorotaKw/test_portfolio/assets/69016457/f5ab7613-0335-4edf-84a5-8e06adda8060)

* . Dla każdego zakupu wyświetl, imię i nazwisko klienta, który dokonał wypożyczenia oraz tytuł wypożyczonego filmu. (wykorzystaj do tego funkcję inner join, zastanów się wcześniej, które tabele Ci się przydadzą do wykonania ćwiczenia).

SELECT name, surname, title FROM sale INNER JOIN customers ON customers.customer_id=sale.customer_id INNER JOIN movies ON movies.movie_id=sale.movie_id;

![sql_14](https://github.com/DorotaKw/test_portfolio/assets/69016457/2f0a29c5-e748-4c31-83f8-71c746d8d835)

* W celu anonimizacji danych, chcesz stworzyć pseudonimy swoich klientów. - Dodaj kolumnę o nazwie ‘pseudonym’ do tabeli customer,- Wypełnij kolumnę w taki sposób, aby pseudonim stworzył się z dwóch pierwszych liter imienia i ostatniej litery nazwiska. Np. Natalie Pilling → Nag

ALTER TABLE customers ADD COLUMN pseudonim varchar(3); UPDATE customers set pseudonim = concat(LEFT(name, 2), RIGHT(surname, 1))

![sql_15](https://github.com/DorotaKw/test_portfolio/assets/69016457/79255353-7e96-406b-8f47-b243cac79830)

* Wyświetl tytuły filmów, które zostały zakupione, wyświetl tabelę w taki sposób, aby tytuły się nie powtarzały.

SELECT DISTINCT movies.title FROM movies INNER JOIN sale on sale.movie_id=movies.movie_id;

![sql_16](https://github.com/DorotaKw/test_portfolio/assets/69016457/c0794c5e-efe6-4c5b-bbb6-c0de3dc1dd0e)

* Wyświetl wspólną listę imion wszystkich aktorów i klientów, a wynik uporządkuj alfabetycznie. (Wykorzystaj do tego funkcji UNION)

SELECT name FROM actors
UNION
SELECT name FROM customers
ORDER BY name ASC

![sql_17](https://github.com/DorotaKw/test_portfolio/assets/69016457/af270ed7-cce7-4b3a-bca6-274dfe5383aa)

* Polskę opanowała inflacja i nasz sklepik z filmami również dotknął ten problem. Podnieś cenę wszystkich filmów wyprodukowanych po 2000 roku o 2,5 $ (Pamiętaj, że dolar to domyślna jednostka- nie używaj jej nigdzie)

UPDATE movies 
SET price=price+2.5 
WHERE year_of_production>2000

![sql_18](https://github.com/DorotaKw/test_portfolio/assets/69016457/c8dcea67-146d-4112-94a1-4a1caa72b95e)

* Wyświetl imię i nazwisko aktora o id 4 i tytuł filmu, w którym zagrał

SELECT actors.actor_id, actors.name, actors.surname, movies.title FROM actors, movies, cast WHERE movies.movie_id = cast.movie_id and actors.actor_id = "4" and cast.actor_id=actors.actor_id;

![sql_19](https://github.com/DorotaKw/test_portfolio/assets/69016457/b556ba2c-1ad9-4702-89b9-70b876e53e59)

* A gdzie nasza HONIA!? Dodaj do tabeli customers nową krotkę, gdzie customer_id = 7, name = Honia, surname = Stuczka-Kucharska, email = honia@mail.com oraz pseudonym = Hoa.

INSERT INTO customers (customer_id, name, surname, email, pseudonym)
VALUES ('7', 'Honia', 'Stuczka-Kucharska', 'honia@mail.com', 'Hoa')

![sql_20](https://github.com/DorotaKw/test_portfolio/assets/69016457/617b1391-c735-4963-bce1-e49f85d177a1)








