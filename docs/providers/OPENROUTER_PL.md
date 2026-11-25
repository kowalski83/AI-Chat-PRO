# OpenRouter

AI Chat PRO integruje OpenRouter z Roblox Studio za pomocą lokalnego programu AI Chat Bridge. Zapytania są realizowane na indywidualnym koncie API użytkownika.

## Funkcjonalność

Pomoc w programowaniu, analiza kodu i wykonywanie zadań agenta w zakresie możliwości wybranego modelu. Obsługa obrazów zależy od modelu i adaptera; limit pluginu wynosi 20 MB łącznie.

## Konfiguracja

1. Uruchom AI Chat Bridge i przejdź do ustawień API.
2. Wybierz OpenRouter i wpisz własny klucz API.
3. Zapisz klucz w Bridge. Tylko przy pierwszym połączeniu skopiuj token parowania do Studio.
4. Wybierz dostawcę i dostępny model z listy dopuszczonych.

Adres API: `https://openrouter.ai/api/v1`.

## Bezpieczeństwo i prywatność

Bridge chroni zapisane klucze przez Windows DPAPI i łączy się z dostawcą przez HTTPS. Kontrola poufnych danych obejmuje wybrane wzorce sekretów, a nie wszystkie dane osobowe. Bridge nie wykonuje dodatkowej moderacji treści tej integracji. Żądania zawierają `data_collection: deny`, co nie gwarantuje zerowej retencji.

Szczegóły: [prywatność](../PRIVACY_POLICY_PL.md), [instalacja](../INSTALLATION_PL.md).

## Rozliczenia

Użytkownik rozlicza wykorzystanie API bezpośrednio z dostawcą. Zakup pluginu nie obejmuje kredytów ani abonamentu AI.

## Dokumentacja dostawcy

[OpenRouter](https://openrouter.ai/docs)

AI Chat PRO jest niezależnym produktem; kompatybilność nie oznacza sponsorowania ani certyfikacji.
