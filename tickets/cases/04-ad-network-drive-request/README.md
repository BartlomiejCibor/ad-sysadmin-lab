# Utworzenie wspólnego dysku sieciowego dla grupy użytkowników  Active Directory — symulacja w homelabie **Otwarte**

## Zgłoszenie

Proszę o utworzenie wspólnego dysku sieciowego dla użytkowników należących do grupy „Logistyka” w domenie Active Directory.
Dysk powinien być automatycznie podłączany po zalogowaniu użytkownika do komputera domenowego.

## Zakres prac

- [x] Utworzenie grupy zabezpieczeń w Active Directory i dodanie wskazanych użytkowników.
- [ ] Utworzenie folderu współdzielonego na serwerze.
- [ ] Skonfigurowanie uprawnień SMB i NTFS.
- [ ] Utworzenie polityki GPO mapującej dysk sieciowy jako `Z:`.
- [ ] Ograniczenie dostępu do zasobu wyłącznie do członków wskazanej grupy AD.
- [ ] Przetestowanie uprawnień odczytu, zapisu i modyfikacji plików.
- [ ] Sprawdzenie automatycznego mapowania dysku po zalogowaniu użytkownika.

## oczekiwany rezultat 

Użytkownicy należący do wskazanej grupy AD mają automatycznie podłączany dysk Z: po zalogowaniu do domeny. Mogą wspólnie odczytywać, tworzyć i edytować pliki. Pozostali użytkownicy nie mają dostępu do zasobu.

## Weryfikacja

Planowane testy:
- Sprawdzenie mapowania dysku `Z:` na koncie użytkownika z grupy „Logistyka”.
- Sprawdzenie możliwości tworzenia, edytowania i usuwania plików.
- Sprawdzenie braku dostępu dla użytkownika spoza grupy.
- Weryfikacja zastosowania polityki GPO.
## Użyte narzędzia


## Zgłoszenie
