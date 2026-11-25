# Moderacja treści

Dla zadań OpenAI API Bridge sprawdza wejście PrivacyGuard, wysyła fragmenty tekstu do OpenAI /v1/moderations z własnym kluczem API klienta przed generowaniem oraz sprawdza zakończony tekst przed przekazaniem go do Studio. Oznaczenie treści lub niedostępny/nieprawidłowy wynik moderacji zatrzymuje zadanie. Załączniki obrazowe OpenAI są obsługiwane z moderacją przed generowaniem; pozostali dostawcy bez tej moderacji treści. Tekst OpenRouter, Groq i lokalnych modeli nie trafia do moderacji OpenAI. Moderacja nie jest weryfikacją wieku, wykrywaniem CSAM ani gwarancją bezpieczeństwa. Dzielenie tekstu może utracić kontekst; odrzucona odpowiedź mogła już naliczyć koszt generowania. Dokumentacja: https://developers.openai.com/api/docs/guides/moderation.

[Obsługa obrazów](IMAGE_SAFETY_PL.md) · [Ograniczenia](KNOWN_LIMITATIONS_PL.md)
