# Model zagrożeń
Chronione zasoby: klucze, token sesji, kod projektu, historia, załączniki, koszty i integralność projektu. Granice zaufania: Studio, HTTP lokalny, konto Windows, HTTPS dostawcy i serwer lokalnej inferencji.

| Zagrożenie | Ochrona / pozostałe ryzyko |
|---|---|
| Dostęp LAN/przeglądarki | Loopback, kontrola host/origin; bez tunelu |
| Lokalny klient bez autoryzacji | Token sesji; malware tego samego użytkownika nadal groźne |
| Kradzież tokenu/klucza | Token w pamięci i DPAPI na dysku; ryzyko schowka i konsoli |
| Złośliwa odpowiedź AI | Walidacja narzędzi i Undo; ryzyko prompt injection i destrukcji |
| Wyciek danych | Ograniczenia dostawców; brak kompletnego skanera sekretów/PII |
| Nieautoryzowane koszty | Własny klucz, ograniczenie równoległości i prób; limity u dostawcy |
| Złośliwy EXE | Budowanie i SHA256; podpis i dystrybucja niezweryfikowane |
| Fałszywy wiek | Samo oświadczenie; niezależna weryfikacja nierozwiązana |

Nie deklarować formalnej gwarancji bezpieczeństwa. Wymagane testy przed wydaniem.
