# Architektura i granice wykonania
Plugin Luau w Roblox Studio obsługuje czat, wybór modelu, zbieranie kontekstu projektu, wywołania narzędzi, modyfikacje projektu, punkty Undo i kolejkę Workera. Bridge Python to lokalny serwer HTTP, nie serwer AI wydawcy. Bridge uwierzytelnia zapytania kluczem klienta, plugin interpretuje odpowiedzi i wykonuje obsługiwane operacje Studio. Bridge nie wykonuje kodu Luau wygenerowanego przez model.

```mermaid
flowchart TD
 S[Plugin Roblox Studio PRO] -->|HTTP loopback + token sesji| B[Windows Bridge]
 B --> V[Magazyn DPAPI użytkownika]
 B --> H[Historia, eksporty, logi]
 B -->|HTTPS własny klucz| O[OpenAI API]
 B -->|HTTPS własny klucz| P[OpenRouter / Groq]
 B -->|prywatny endpoint| L[LM Studio / Ollama]
 F[FREE planowany - SIWC wyłączone] -. przyszła integracja .-> B
```
Worker mieści do 30 zadań w pamięci sesji Studio. Po sukcesie zamykany jest punkt Undo i następuje 30 s przerwy. Jawne błędy 502/503/504 mogą być ponawiane, lecz nie całe zadania ani częściowe generacje. Błąd końcowy zatrzymuje kolejkę. Failover nie jest wdrożony. Undo nie jest pełną kopią dyskową; eksport pomija część geometrii. W sprawdzonych źródłach nie ma serwera telemetrii wydawcy.
