# Brak dostępu do stron internetowych  — symulacja w homelabie **Rozwiązane**

## Zgłoszenie
Użytkowniczka Agnieszka zgłosiła problem z wyświetlaniem stron internetowych. ![Zgłoszony problem w przeglądarce](images/internet-problem.png)  Użytkowniczka  używa przeglądarki Edge, kolega z pracy zasugerował sprawdzenie w wierszu poleceń komendy pingującej widocznej na zdjęciu powyżej.

## Diagnoza
Zrzut ekranu pokazuje że ping 1.1.1.1 działa poprawnie, aczkolwiek ping do strony internetowej na przykład google.com już nie działa. ![Wyniki wstępnych testów](images/ping-request.png) Klientka napisała mi, że na komputerze koleżanki strony internetowe wyświetlają się poprawnie, sprawdziłem ustawienia i okazało się że DNS nie jest poprawnie skonfigurowany na komputerze użytkowniczki (Agnieszka). 

## Przyczyna
Przyczyną problemu jest zła konfiguracja DNS na komputerze użytkowniczki, jako DNS ustawiony był adres 10.0.40.231.


## Działanie
Sprawdziłem adres serwera DNS skonfigurowany na komputerze użytkowniczki Agnieszka. Zamiast właściwego serwera DNS domeny lab.local (10.0.40.10) skonfigurowany był adres 10.0.40.231. Zmieniłem ustawienie DNS na 10.0.40.10, a następnie sprawdziłem działanie stron internetowych.
![Konfiguracja sieci przed zmianą](images/internet-settings.png)

## Weryfikacja
Potwierdziłem, że strony internetowe uruchamiają się poprawnie a nazwa google.com jest rozpoznawana. ![Strona otwarta po naprawie](images/internet-browser-confirmation.png) ping google.com także działa poprawnie ![Test po naprawie](images/ping-google.png)


## Użyte narzędzia
GLPI, serwer DNS domeny lab.local, ping 
