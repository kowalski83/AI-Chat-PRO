# OpenAI API

AI Chat PRO integruje OpenAI API z Roblox Studio za pomocą lokalnego programu AI Chat Bridge. Zapytania są realizowane na indywidualnym koncie API użytkownika.

## Funkcjonalność

Pomoc w programowaniu, analiza kodu i wykonywanie zadań agenta w zakresie możliwości wybranego modelu. Obsługa obrazów zależy od modelu i adaptera; limit pluginu wynosi 20 MB łącznie.

## Konfiguracja

1. Zatrzymaj Bridge i uruchom `KONFIGURUJ_KLUCZE.bat`.
2. Wybierz OpenAI API i wpisz własny klucz API.
3. Uruchom Bridge i wprowadź token sesji w Studio.
4. Wybierz dostawcę i dostępny model z listy dopuszczonych.

Adres API: `https://api.openai.com/v1`.

## Bezpieczeństwo i prywatność

Bridge chroni zapisane klucze przez Windows DPAPI i łączy się z dostawcą przez HTTPS. Kontrola poufnych danych obejmuje wybrane wzorce sekretów, a nie wszystkie dane osobowe. Moderacja obejmuje tekst i obsługiwane obrazy przed generowaniem oraz tekst odpowiedzi po generowaniu. Odrzucenie treści lub błąd moderacji zatrzymuje zadanie. Ustawienie `store: false` nie gwarantuje zerowej retencji. Moderacja nie potwierdza wieku.

Szczegóły: [prywatność](../PRIVACY_POLICY_PL.md), [instalacja](../INSTALLATION_PL.md).

## Rozliczenia

Użytkownik rozlicza wykorzystanie API bezpośrednio z dostawcą. Zakup pluginu nie obejmuje kredytów ani abonamentu AI.

## Dokumentacja dostawcy

[OpenAI API](https://developers.openai.com/api/docs)

AI Chat PRO jest niezależnym produktem; kompatybilność nie oznacza sponsorowania ani certyfikacji.
