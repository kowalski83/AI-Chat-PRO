# GroqCloud

AI Chat PRO integruje GroqCloud z Roblox Studio za pomocą lokalnego programu AI Chat Bridge. Zapytania są realizowane na indywidualnym koncie API użytkownika.

## Funkcjonalność

Pomoc w programowaniu, analiza kodu i wykonywanie zadań agenta w zakresie możliwości wybranego modelu. Obsługa obrazów zależy od modelu i adaptera; limit pluginu wynosi 20 MB łącznie.

## Konfiguracja

1. Uruchom AI Chat Bridge i przejdź do ustawień API.
2. Wybierz GroqCloud i wpisz własny klucz API.
3. Zapisz klucz w Bridge. Tylko przy pierwszym połączeniu skopiuj token parowania do Studio.
4. Wybierz dostawcę i dostępny model z listy dopuszczonych.

Adres API: `https://api.groq.com/openai/v1`.

## Bezpieczeństwo i prywatność

Bridge chroni zapisane klucze przez Windows DPAPI i łączy się z dostawcą przez HTTPS. Kontrola poufnych danych obejmuje wybrane wzorce sekretów, a nie wszystkie dane osobowe. Bridge nie wykonuje dodatkowej moderacji treści tej integracji.

Szczegóły: [prywatność](../PRIVACY_POLICY_PL.md), [instalacja](../INSTALLATION_PL.md).

## Rozliczenia

Użytkownik rozlicza wykorzystanie API bezpośrednio z dostawcą. Zakup pluginu nie obejmuje kredytów ani abonamentu AI.

## Dokumentacja dostawcy

[GroqCloud](https://console.groq.com/docs/overview)

AI Chat PRO jest niezależnym produktem; kompatybilność nie oznacza sponsorowania ani certyfikacji.
