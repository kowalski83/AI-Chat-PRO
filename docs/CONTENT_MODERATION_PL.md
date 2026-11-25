# Planowane zabezpieczenia treści i prywatności
Niewdrożone w kandydacie: dedykowana moderacja zapytań i zakończonych odpowiedzi, kompleksowy skaner danych osobowych/sekretów, UI zgłoszeń, zweryfikowany wiek i pełne usuwanie historii. Plan: kontrola przed wysłaniem (kontekst i załączniki), blokada oczywistych sekretów, odpowiednio autoryzowana moderacja, zatrzymanie oznaczonej odpowiedzi przed wykonaniem narzędzi, bezpieczne wyjaśnienie i prywatny kanał zgłoszeń. Nie przekazywać po cichu danych klientów innego dostawcy do OpenAI w celu moderacji; ujawnić przepływ i uzyskać odpowiednie upoważnienie. Nie logować odrzuconych treści. Zdefiniować obsługę awarii i testy błędnych klasyfikacji. Moderacja nie weryfikuje wieku ani nie gwarantuje prywatności.


## Stage 2 / Etap 2
Etap 2 wprowadza podstawowy filtr regex tekstu wysyłanego do chmury (w tym kontekstu) i zakończonych odpowiedzi: e-mail, wybrane wzorce sekretów i aktywny klucz. Dopasowania są blokowane, bez wysyłania do dodatkowego dostawcy moderacji. Obrazy i dowolne dane osobowe nie są objęte. Możliwe fałszywe alarmy i przeoczenia. Pełna moderacja, niezależna weryfikacja wieku i zgłoszenia pozostają do wdrożenia.
