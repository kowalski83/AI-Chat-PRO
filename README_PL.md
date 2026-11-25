# AI Chat PRO / AI Chat FREE — dokumentacja do oceny technicznej
**Dokumentacja do konsultacji technicznej — PRO 4.9.35, kandydat SECURITY etap 3.** Publikacja produktu jest odrębną decyzją; testy natywne pozostają otwarte. Wydawca: kowalski83. Niezależne oprogramowanie, bez certyfikacji lub rekomendacji OpenAI i Roblox.

PRO 4.9.35 wykorzystuje własne klucze API klientów oraz lokalne serwery modeli. FREE 4.9.36 to planowany niezależny darmowy plugin; dostęp subskrypcyjny i Codex nie są wdrożone ani autoryzowane. Wspólny darmowy Bridge jest planowany, lecz rozdzielenie uprawnień edycji nie jest jeszcze wdrożone.

Podstawa techniczna: źródła 4.9.35 Worker/Retry/Logs z tokenem sesji, lokalną konfiguracją kluczy i podstawową kontrolą tekstu. Natywny EXE, UI Studio, rzeczywiste API i weryfikacja wieku pozostają niezweryfikowane. Obecny publiczny EXE może różnić się od tej wersji.

## Spis dokumentacji
- [AGE_SAFETY_PL](docs/AGE_SAFETY_PL.md)
- [API_KEY_SECURITY_PL](docs/API_KEY_SECURITY_PL.md)
- [ARCHITECTURE_PL](docs/ARCHITECTURE_PL.md)
- [BRIDGE_PROTOCOL_PL](docs/BRIDGE_PROTOCOL_PL.md)
- [CONTENT_MODERATION_PL](docs/CONTENT_MODERATION_PL.md)
- [DATA_FLOW_PL](docs/DATA_FLOW_PL.md)
- [FREE_VS_PRO_PL](docs/FREE_VS_PRO_PL.md)
- [INSTALLATION_PL](docs/INSTALLATION_PL.md)
- [KNOWN_LIMITATIONS_PL](docs/KNOWN_LIMITATIONS_PL.md)
- [OPENAI_INTEGRATION_PL](docs/OPENAI_INTEGRATION_PL.md)
- [PRIVACY_POLICY_PL](docs/PRIVACY_POLICY_PL.md)
- [PROVIDER_COMPLIANCE_PL](docs/PROVIDER_COMPLIANCE_PL.md)
- [SIWC_INTEGRATION_PL](docs/SIWC_INTEGRATION_PL.md)
- [THREAT_MODEL_PL](docs/THREAT_MODEL_PL.md)

[English README](README.md)

- [Security tests / Testy bezpieczeństwa](docs/SECURITY_TESTS_PL.md)


Regresja etapu 2: 249 zaliczonych, 2 pominięte. Dokumentacja do konsultacji technicznych; walidacja wydania handlowego pozostaje odrębnym zadaniem.


## Etap 3 — aktualny kandydat
Tylko dla zadań tekstowych OpenAI API Bridge sprawdza wejście dotychczasowym PrivacyGuard, wysyła fragmenty tekstu do OpenAI /v1/moderations z własnym kluczem API klienta przed generowaniem oraz sprawdza zakończony tekst przed przekazaniem go do Studio. Oznaczenie treści lub niedostępny/nieprawidłowy wynik moderacji zatrzymuje zadanie. Załączniki obrazowe w zadaniach OpenAI są zablokowane; pozostali dostawcy pozostają bez nowej moderacji treści. Tekst OpenRouter, Groq i lokalnych modeli nie trafia do moderacji OpenAI. Moderacja nie jest weryfikacją wieku, wykrywaniem CSAM ani gwarancją bezpieczeństwa. Dzielenie tekstu może utracić kontekst; odrzucona odpowiedź mogła już naliczyć koszt generowania. Dokumentacja: https://developers.openai.com/api/docs/guides/moderation.

Lokalną historię można wyłączyć przy starcie przez AI_CHAT_HISTORY_DISABLED=1 lub URUCHOM_BEZ_HISTORII.bat; w tym trybie wszystkie endpointy HTTP historii są blokowane. Nie usuwa to istniejących plików ani nie wyłącza kontekstu w pamięci, eksportów, logów diagnostycznych i retencji dostawcy. Po zamknięciu wszystkich instancji Studio i Bridge uruchom USUN_HISTORIE_CZATU.bat lub Bridge --purge-chat-history; wpisz DELETE ALL CHAT HISTORY. Usuwa rozpoznane lokalne pliki JSON historii i nazwane kopie czatów, nie kopie projektów, zewnętrzne kopie importów ani dane dostawcy. To zwykłe usuwanie plików, nie bezpieczne wymazywanie nośnika. Nierozpoznane/uszkodzone pliki mogą wymagać ręcznej kontroli. UI zgłoszeń, niezależna weryfikacja wieku, kompleksowa ochrona danych osobowych, moderacja pozostałych dostawców i obrazów oraz natywne testy Windows i Studio nadal pozostają do wykonania.
