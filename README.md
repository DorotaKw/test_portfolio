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
