# Polityka prywatności — AI Chat PRO / Bridge
**Projekt do uzupełnienia przez wydawcę przed sprzedażą.** Wersja 4.9.35; 24.11.2026.
Wydawca: kowalski83. **Uzupełnij przed publikacją: rzeczywista nazwa/imię i nazwisko, adres kontaktowy, e-mail, dane administratora w zakresie, w jakim przetwarza dane.** Repozytorium: https://github.com/kowalski83/AI-Chat-PRO.

## Przepływ danych
Plugin komunikuje się z Bridge przez 127.0.0.1:8765. Bridge nie zawiera w sprawdzonych źródłach serwera telemetrii wydawcy. Gdy wybierzesz usługę chmurową, Bridge wysyła do wybranego dostawcy prompt, historię/kontekst, fragmenty kodu projektu i ewentualne załączniki zgodnie z używaną funkcją. Klucze służą do uwierzytelniania u właściwego dostawcy. LM Studio / Ollama korzysta ze skonfigurowanego adresu lokalnego lub prywatnej sieci; operator tego serwera odpowiada za dalsze przetwarzanie. CLI oraz Gemini, Cline Cloud, NVIDIA i Devin są wyłączone w Store. Nie przesyłaj tajemnic, danych osobowych innych osób ani materiałów, których nie masz prawa udostępniać.

## Odbiorcy i cele
OpenAI API, OpenRouter, GroqCloud oraz skonfigurowany lokalny LM Studio / Ollama — dostarczanie odpowiedzi AI. Jeśli skonfigurowano Asset ID, identyfikator konta Roblox i zasobu trafiają do inventory.roblox.com w celu informacyjnej kontroli własności. Roblox obsługuje sprzedaż, a GitHub pobieranie pliku; stosują własne warunki i polityki prywatności. Dostawcy mogą przetwarzać dane poza EOG, stosować własne okresy retencji i warunki wykorzystania danych. Sprawdź je przed wyborem modelu. Wydawca nie powinien deklarować kontroli nad tymi procesami.

## Dane lokalne, retencja, usuwanie
Klucze: %APPDATA%/RobloxStudioAIChatAgent/api_keys.json, na Windows DPAPI konta użytkownika (działanie wymaga testu na Windows); wcześniejsze pliki są migrowane przy odczycie. Klucze ze zmiennych środowiskowych pozostają poza tym mechanizmem. Historia: Documents/RobloxStudioChatHistory; eksport: Documents/RobloxStudioExports, o ile nie zmieniono ścieżek; kopie zapasowe w katalogach historii. Załączniki i zadania mogą istnieć w pamięci Bridge podczas sesji. Dane lokalne pozostają do ręcznego usunięcia lub działania odpowiednich funkcji; wyczyszczenie czatu tworzy kopię zapasową, więc nie usuwa wszystkich kopii. Klucze usuń w lokalnej konsoli Bridge (--configure-keys po zatrzymaniu Bridge); usuń również zmienne środowiskowe, jeśli były używane. Po zamknięciu Bridge można ręcznie usunąć potrzebne pliki, w tym kopie i eksporty. Dane zapisane przez dostawców usuwa się według ich zasad.

## Bezpieczeństwo i prawa
Bridge nasłuchuje wyłącznie na loopback; Bridge wymaga losowego tokenu sesji oprócz publicznego nagłówka; nie chroni przed wszystkimi procesami tego samego użytkownika. Używaj tylko na zaufanym komputerze. Nie publikuj portu w sieci. Dane przetwarzane przez wydawcę (np. zgłoszenia pomocy) wymagają ustalenia podstawy prawnej, retencji, odbiorców i kontaktu przed publikacją; w zakresie mającym zastosowanie przysługują prawa dostępu, sprostowania, usunięcia, ograniczenia, przenoszenia, sprzeciwu i skargi do organu nadzorczego. Nie ogranicza to praw użytkownika względem Roblox, GitHub ani dostawców AI. Wydawca musi potwierdzić rzeczywiste praktyki obsługi zgłoszeń i uzupełnić te informacje przed publikacją.

## Zasady danych Roblox i wiek
Nie przekazuj dostawcom AI danych identyfikujących użytkowników Roblox ani danych użytkowników do celów trenowania AI. OpenRouter otrzymuje ustawienie data_collection: deny; nie stanowi to gwarancji zerowej retencji. Sprawdź zasady i ustawienia wybranego konta dostawcy. Program nie rozpoznaje automatycznie wszystkich danych osobowych w dowolnym kodzie lub załączniku. Deklaracja 18+ jest zapamiętywana na czas sesji, przesyłana do lokalnego Bridge i nie jest niezależną weryfikacją wieku. Nie zbieramy dokumentów tożsamości ani daty urodzenia w tym mechanizmie. Gemini pozostaje zablokowane niezależnie od deklaracji.


OpenAI API korzysta z własnego klucza klienta, odrębnych rozliczeń API i ustawienia `store: false`; nie gwarantuje to zerowej retencji. Logowanie subskrypcyjne ChatGPT jest wyłączone. Ollama musi być skonfigurowana wyłącznie do lokalnej inferencji; operator musi wyłączyć funkcje chmurowe. Sam adres lokalny/prywatny nie gwarantuje lokalnego przetwarzania.


## Kolejka Workera i logi diagnostyczne
Kolejka zawiera prompty i przypisane załączniki w pamięci bieżącej sesji Studio. Uruchomione zadania korzystają z dotychczasowych zasad historii i wysyłania danych do dostawcy. Bridge zapisuje lokalnie metadane diagnostyczne (czas, dostawca, operacja, zdarzenie, kod HTTP, numer próby, identyfikator zadania i czas do ponowienia) w Logs/errors.log w katalogu historii. Ten log nie zapisuje surowej treści promptów, kluczy, kodu ani odpowiedzi dostawcy. Rotacja: 1 000 000 bajtów i cztery kopie. Logi nie są automatycznie wysyłane do wydawcy; po zamknięciu Bridge można je usunąć ręcznie.


## Zarządzanie historią

Zobacz [instrukcję zarządzania historią](HISTORY_PL.md) oraz [opis moderacji](CONTENT_MODERATION_PL.md). Obrazy są oczyszczane z metadanych, ale widoczne dane osobowe nie są automatycznie usuwane.
