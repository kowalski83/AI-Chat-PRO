# Historia rozmów

## Wyłączenie zapisu

Przed uruchomieniem Bridge ustaw `AI_CHAT_HISTORY_DISABLED=1` lub użyj `URUCHOM_BEZ_HISTORII.bat`. Tryb blokuje operacje historii przez HTTP, ale nie usuwa istniejących plików ani nie wyłącza kontekstu w pamięci, eksportów, logów i retencji dostawcy.

## Usuwanie

Zamknij wszystkie instancje Studio i Bridge. Uruchom `USUN_HISTORIE_CZATU.bat` lub Bridge z `--purge-chat-history`, a następnie wpisz `DELETE ALL CHAT HISTORY`. Usuwane są rozpoznane archiwa JSON i nazwane kopie czatów, nie kopie projektów ani zewnętrzne eksporty. Jest to zwykłe usunięcie plików, nie bezpieczne wymazanie nośnika. Nierozpoznane pliki mogą wymagać ręcznego usunięcia.

Zasady danych dostawców opisano w [polityce prywatności](PRIVACY_POLICY_PL.md).
