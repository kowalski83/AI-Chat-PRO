# Ollama

AI Chat PRO integruje Ollama z Roblox Studio za pomocą lokalnego programu AI Chat Bridge. Modele uruchamia użytkownik na własnym serwerze.

## Funkcjonalność

Pomoc w programowaniu, analiza kodu i wykonywanie zadań agenta w zakresie możliwości wybranego modelu. Obsługa obrazów zależy od modelu i adaptera; limit pluginu wynosi 20 MB łącznie.

## Konfiguracja

1. Uruchom Ollama i załaduj zgodny model.
2. Uruchom lokalny serwer API.
3. W ustawieniach Bridge ustaw adres `http://127.0.0.1:11434/v1`.
4. Odśwież listę modeli i wybierz model.

## Bezpieczeństwo i prywatność

Adapter lokalny nie wymaga klucza chmurowego. Używaj zaufanego serwera; adres prywatny nie gwarantuje lokalnego przetwarzania. Bridge nie wykonuje dodatkowej moderacji treści tego adaptera. Wyłącz funkcje chmurowe Ollama; integracja korzysta ze wspólnego adaptera lokalnego.

Szczegóły: [prywatność](../PRIVACY_POLICY_PL.md), [instalacja](../INSTALLATION_PL.md).

## Rozliczenia

Koszty sprzętu, energii i ewentualnych licencji modeli ponosi użytkownik.

## Dokumentacja dostawcy

[Ollama](https://docs.ollama.com/)

AI Chat PRO jest niezależnym produktem; kompatybilność nie oznacza sponsorowania ani certyfikacji.
