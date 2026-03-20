# Mobile Extension — Optional Micro-Support (10–15 min, not core track)

## Cel
Dać uczestnikom zainteresowanym mobile krótki, realistyczny most z głównego toru kursu (web + backend) do ich pracy, bez zamiany szkolenia w warsztat mobile.

## Kiedy użyć
- Tylko jeśli grupa zgłasza realną potrzebę mobile (np. ankieta / pytania na żywo).
- Najlepsze okno: Day 5, blok końcowy (warsztat mini-playbook), jako dodatek dla chętnych.
- Jeśli czasu brakuje: traktuj jako "co dalej" po kursie.

## Ramy 10–15 minut
1. **2 min — ustawienie oczekiwań**
   - "To nie jest pełny moduł mobile, tylko mapa adaptacji."
2. **4–5 min — wzorzec przeniesienia z toru głównego**
   - Ten sam backend API, te same guardraile, inne UI i nawigacja.
   - Ten sam workflow agentowy: prompt → diff → test → review.
3. **4–5 min — mikro-ćwiczenie projektowe**
   - Uczestnik wybiera 1 flow z kursowej aplikacji i opisuje wersję mobile:
     - ekran(y),
     - walidacje,
     - stany błędów,
     - telemetry/logowanie.
4. **2–3 min — ryzyka i scope control**
   - Nie robimy pełnej implementacji mobile podczas kursu.
   - Priorytet: działający i bezpieczny workflow w głównym torze.

## Gotowiec do wklejenia na chat
```text
Opcjonalny most do mobile (10–15 min):
- użyj tego samego backendu i zasad bezpieczeństwa,
- zaprojektuj 1 mobilny flow (ekrany + walidacje + błędy),
- opisz jak ten sam workflow AI (prompt → diff → test → review) działa w mobile.
To dodatek dla chętnych, nie rdzeń kursu.
```

## Kryteria jakości (dla trenera)
- Uczestnik umie nazwać co najmniej 2 elementy "1:1" z toru web/backend do mobile.
- Uczestnik umie wskazać 1 element, który musi zmienić pod mobile (UX/performance/offline/bezpieczeństwo).
- Czas modułu nie przekracza 15 min i nie narusza głównych artefaktów Day 5.

## Why this matters (dla trenera)
- Odpowiadamy na potrzebę z ankiety bez rozbijania głównego celu kursu.
- Utrzymujemy spójność: jeden główny workflow, rozszerzenia tylko jako kontrolowane dodatki.
