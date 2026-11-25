# Transport lokalny
Domyślnie 127.0.0.1:8765; port QWEN_BRIDGE_PORT. Kontrola Host, Origin i Fetch Metadata ogranicza typowe żądania przeglądarkowe. Publiczny GET /health zwraca minimalne metadane. Chronione endpointy wymagają nagłówka edycji ORAZ losowego tokenu sesji 256-bitowego. Token jest celowo wyświetlany w interaktywnej konsoli, wklejany w panelu Studio, przechowywany w pamięci modułu i wymieniany po restarcie Bridge. HTTP nie zwraca tokenu. /auth/* nie jest API parowania. Lokalny HTTP nie jest TLS. Nie wystawiaj portu ani nie tuneluj. Token nie weryfikuje licencji ani tożsamości systemowej. Pozostają ryzyka procesów tego samego użytkownika, schowka, złośliwego pluginu i podszycia pod port. Wymagane testy Windows i Studio.

Endpointy obejmują dostawców, modele, zadania, anulowanie, konfigurację kluczy i lokalnego endpointu, historię, załączniki, eksporty i rejestr kopii. Token nie izoluje okien Studio od siebie. Metadane /health nie dowodzą autentyczności serwera.


POST /config/api-key odrzuca zapis kluczy (403); /config/api-status pozostaje tylko do odczytu.
