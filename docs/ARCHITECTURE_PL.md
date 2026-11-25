# Architektura
Plugin Roblox Studio obsługuje interfejs, kontekst projektu i operacje edycji. Lokalny Bridge pośredniczy w połączeniach z wybranymi dostawcami; nie jest centralnym serwerem AI wydawcy. Klient rozlicza API bezpośrednio z dostawcą. Worker obsługuje kolejkę zadań i punkty Undo; nie zastępują one pełnej kopii projektu.
