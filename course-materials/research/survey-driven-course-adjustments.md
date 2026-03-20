# Survey-driven Course Adjustments (NBP, 2026-03-16)

## Cel pliku
Przełożyć odpowiedzi z ankiety pre-course na konkretne decyzje wykonawcze dla kursu 5-dniowego.

## Źródło
- `materials/references/nbp-precourse-survey-2026-03-16.md`
- Kontekst programu: `materials/references/jsystems-program-ai-od-pomyslu-do-mvp.md`

## Szybki profil grupy (z ankiety)
- Liczba odpowiedzi: 3
- Poziom: 2x beginner, 1x intermediate
- Stack: Java + SQL, środowisko Windows, IntelliJ jako główne IDE
- Kontekst enterprise/bankowy: Jira + Jenkins + GitHub (on-prem), Argo CD/Kubernetes
- Potrzeby: praktyka narzędzi AI, bezpieczny AI SDLC, porównanie workflow, ograniczanie ryzyka

---

## Decyzja 1 — Kontekst on-prem (Jenkins + GitHub + Argo)

### Co zmieniamy w kursie
1. **Każdy blok „cloud max” dostaje sekcję „adaptacja on-prem/local”.**
2. W Day 3–5 używamy stałego wzorca porównania:
   - wariant A: cloud (szybki start, większa wygoda),
   - wariant B: enterprise/on-prem (kontrola, zgodność, audyt).
3. W materiałach i skryptach trenera dokładamy checklistę pytań wdrożeniowych:
   - gdzie działa model (cloud/self-hosted),
   - gdzie trafiają logi/prompty,
   - kto zatwierdza merge/deploy,
   - jak działa rollback i ślad audytowy.

### Dlaczego
- Uczestnicy pracują w środowiskach regulowanych i już wskazali Jenkins/Jira/GitHub/Argo.
- Kurs ma być „jutro do użycia”, a nie tylko „demo w chmurze”.

### Konkretne wpięcie do planu
- Day 4 (CI/CD) i Day 5 (utrzymanie/operacjonalizacja): obowiązkowy mini-segment „cloud vs on-prem” z tym samym use casem.
- Do przygotowania osobny materiał badawczy (TODO G1/G2): realistyczne przykłady pipeline i approvals.

---

## Decyzja 2 — Mieszany poziom beginner/intermediate

### Co zmieniamy w kursie
1. **Dwa tory ćwiczeń** w każdym dniu pozostają obowiązkowe:
   - Core (ukończenie przez każdego),
   - Stretch (dla szybszych/intermediate).
2. Każdy większy moduł zaczyna się od krótkiego „minimum theory” (5–10 min),
   potem natychmiast przejście do praktyki artefaktowej.
3. Wprowadzamy stały rytm kontroli tempa:
   - sygnał kciuk/reaction co 20–30 min,
   - szybkie checkpointy „co działa / co blokuje”.

### Dlaczego
- Grupa jest nierówna poziomem; bez torów część uczestników będzie się nudzić, a część zgubi tempo.
- Ankieta pokazuje duże zapotrzebowanie na uporządkowany workflow, nie tylko na „wow demo”.

### Konkretne wpięcie do planu
- Utrzymać i doprecyzować mapowanie Core/Stretch w `exercises/03-exercises.md`.
- W skryptach dziennych dopisać jawne checkpointy adaptacji (tempo + decyzja: jedziemy dalej / robimy mikro-powtórkę).

---

## Decyzja 3 — Priorytet bezpieczeństwa

### Co zmieniamy w kursie
1. **Bezpieczeństwo jako oś kursu, nie dodatek na końcu.**
2. Dwa jawne punkty kontrolne (must-have):
   - audyt legacy JFTP (ryzyka + plan naprawczy),
   - audyt końcowej aplikacji (sekrety, walidacja, nadużycia, prompt-injection/data leakage).
3. W każdym dniu utrzymujemy krótką sekcję „ryzyko + guardrail” w kontekście bieżącego modułu.

### Dlaczego
- Respondenci wprost wskazali security analysis i risk assessment jako kluczowe cele.
- Kontekst bankowy wymaga audytowalności i defensywnego workflow AI.

### Konkretne wpięcie do planu
- Zaszyć checkpointy bezpieczeństwa w Day 4 + Day 5 i w `exercises/03-exercises.md` (TODO D4).
- Spiąć z modułem sandbox/safety (już dodanym) jako praktyczny fundament pracy z agentami.

---

## Ramy komunikacyjne dla trenera
- Mówimy językiem praktyki: „co wdrożysz od jutra”, „co zmniejsza ryzyko”, „co przechodzi audyt”.
- Nie obiecujemy pełnej autonomii; promujemy model: **Plan → Execute → Verify → Approve**.
- Każdy materiał porównawczy cloud/on-prem ma pokazywać kompromisy (szybkość vs kontrola).

## Kryterium akceptacji tego dokumentu
Plik jest gotowy, jeśli zawiera:
- jawne decyzje dla on-prem,
- jawne decyzje dla mixed-level grupy,
- jawne decyzje dla security-first delivery,
- mapowanie tych decyzji na istniejące TODO i artefakty kursu.