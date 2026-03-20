# J2 — Mapowanie programu JSystems do skryptów Day 1–Day 5 (NBP)

Status: draft do użycia w retrofitach J3–J6  
Data: 2026-03-16  
Źródło programu (kontrakt): `materials/references/jsystems-program-ai-od-pomyslu-do-mvp.md`

## Cel
Ustalić jawne mapowanie: **moduł programu JSystems → konkretne sekcje w skryptach dziennych NBP**.  
To jest plik śledzenia zgodności kontraktowej (traceability), który będzie referencją przy retrofitach J3–J6.

---

## Day 1 — Fundamenty i misja

### JSystems 1.1 — The New Frontier
- Zakres programu: mindset AI-first, mity, korzyści/ryzyka, wpływ AI na pracę developera.
- Pokrycie w skrypcie NBP (`materials/scripts/day-1-script.md`):
  - `10:00–10:25 — Mission kickoff: po co ten tydzień i po co ten workflow`
  - `14:15–14:30 — Review loop: generated draft ≠ truth`
  - `15:20–15:45 — ... bezpieczeństwa: sandbox, WSL, bash vs PowerShell`
- Ocena: **Pokryte** (mindset + ryzyka + kontrola jakości/safety).

### JSystems 1.2 — Kluczowe koncepcje: modele, prompty, vibe coding
- Zakres programu: modele, tokeny, kontekst, prompt engineering, balans automatyzacja/kontrola.
- Pokrycie w skrypcie NBP:
  - `09:40–10:00 — Anonimowy quiz AI basics` (fundamenty pojęciowe)
  - `10:25–11:00 — Codex-first safe setup + pierwszy mały sukces`
  - `12:05–13:00 — PRD + AGENTS mini-workshop`
- Ocena: **Pokryte** (fundament + prompting + kontrola procesu).

### JSystems 1.3 — Mission Briefing & przygotowanie środowiska
- Zakres programu: setup narzędzi i środowiska, wybór projektu, high-level arch.
- Pokrycie w skrypcie NBP:
  - `10:25–11:00 — Codex-first safe setup + pierwszy mały sukces`
  - `11:15–11:35 — Krótkie porównanie: Codex vs Claude vs IntelliJ AI Assistant`
  - `14:40–15:20 — mini-moduł WezTerm`
- Ocena: **Pokryte** (Codex-first + porównanie narzędzi + ergonomia terminala).

### JSystems 1.4 — AI Research i wymagania projektu
- Zakres programu: research, walidacja pomysłu, plan projektu (README/user stories/roadmapa/stack).
- Pokrycie w skrypcie NBP:
  - `11:35–12:05 — Projekt tygodnia i zakres MVP`
  - `12:05–13:00 — PRD + AGENTS mini-workshop`
  - `13:30–14:15 — Pierwszy widoczny artefakt repo`
- Ocena: **Pokryte**.

---

## Day 2 — Od pomysłu do projektu

### JSystems 2.1 — Advanced Research & planowanie projektu
- Zakres programu: wybór bibliotek/frameworków, struktura projektu, architektura.
- Pokrycie w skrypcie NBP (`materials/scripts/day-2-script.md`):
  - `09:20–10:05 — Problem framing`
  - `10:05–11:00 — Założenia, ograniczenia i kryteria akceptacji`
  - `11:15–12:05 — Architektura wysokiego poziomu`
  - `14:20–14:30 — ADR: decyzje architektoniczne i kompromisy`
- Ocena: **Pokryte**.

### JSystems 2.2 — AI-Powered UX/UI Design
- Zakres programu: AI-native design, prototyping (Lovable/v0/Bolt/Figma), klikalny prototyp.
- Pokrycie w skrypcie NBP:
  - `13:30–14:20 — UX/UI prototyping i przejście z ekranu do zadań dla AI`
- Ocena: **Pokryte (adaptacja)** — nacisk na workflow „prototyp → zadania dla agenta” zamiast narzędzio-centrycznego przeglądu wielu platform.

### JSystems 2.3 — From Design to Code
- Zakres programu: translacja prototypu do kodu FE (statyczne komponenty).
- Pokrycie w skrypcie NBP:
  - `13:30–14:20 — UX/UI prototyping...`
  - `15:25–16:00 — Task slicing + handoff do Day 3` (przygotowanie implementacji)
- Ocena: **Pokryte (z handoffem)**.

---

## Day 3 — Budowa rdzenia aplikacji

### JSystems 3.1 — Poznaj swoje AI-Powered IDE
- Zakres programu: Codex/Codex CLI jako główna ścieżka, porównania, integracja terminala.
- Pokrycie w skrypcie NBP (`materials/scripts/day-3-script.md`):
  - `09:00–09:20 — Handoff z Day 2...`
  - `14:20–14:30 — Krótkie porównanie: Codex vs Claude vs IntelliJ + mikro‑moduł WezTerm`
- Ocena: **Pokryte**.

### JSystems 3.2 — Full-Stack Generation & CLI Power
- Zakres programu: generowanie backendu API, połączenie FE+BE, praca z CLI.
- Pokrycie w skrypcie NBP:
  - `09:20–10:05 — backend skeleton + kontrakt`
  - `10:05–11:00 — warstwa danych`
  - `11:15–12:05 — UI + przepływ end-to-end`
  - `12:05–13:00 — pętla iteracji: diff/test/poprawka/commit`
- Ocena: **Pokryte**.

### JSystems 3.3 — AI-Assisted Debugging & Refactoring
- Zakres programu: diagnoza błędów, stack trace do AI, refaktoryzacja.
- Pokrycie w skrypcie NBP:
  - `13:30–14:20 — Debugging z AI`
  - `14:40–15:25 — Refaktoryzacja i porządkowanie kodu`
- Ocena: **Pokryte**.

---

## Day 4 — Jakość, bezpieczeństwo i wdrożenie

### JSystems 4.1 — AI-Generated Testing
- Zakres programu: testy unit/integration/E2E i ich ograniczenia.
- Pokrycie w skrypcie NBP (`materials/scripts/day-4-script.md`):
  - `09:20–10:05 — Testy z AI`
  - `14:40–15:25 — Warsztat naprawczy` (domykanie po testach)
- Ocena: **Pokryte**.

### JSystems 4.2 — Automated Code Reviews & Security
- Zakres programu: AI code review + security scanning.
- Pokrycie w skrypcie NBP:
  - `10:05–11:00 — Review wygenerowanego kodu`
  - `11:15–12:05 — Security i audyt`
- Ocena: **Pokryte** (w tym checkpointy audytowe).

### JSystems 4.3 — AI for CI/CD and Automation
- Zakres programu: pipeline i wdrożenie z AI.
- Pokrycie w skrypcie NBP:
  - `13:30–14:20 — CI/CD i automatyzacja: cloud-max vs on-prem`
  - wsparcie: `materials/research/cicd-agent-workflows-cloud-vs-onprem.md`
- Ocena: **Pokryte**.

---

## Day 5 — Mistrzostwo, utrzymanie i przyszłość

### JSystems 5.1 — Praca ze starym kodem
- Zakres programu: analiza/dokumentacja/refaktoryzacja legacy.
- Pokrycie w skrypcie NBP (`materials/scripts/day-5-script.md`):
  - `10:05–11:00 — Decyzje techniczne i kompromisy` (obrona decyzji)
  - `14:40–15:25 — Warsztat końcowy: mini-playbook`
  - + wcześniejszy kontekst legacy z Day 4 jako ciągłość dydaktyczna.
- Ocena: **Pokryte (rozciągnięte Day4→Day5)**.

### JSystems 5.2 — Modele lokalne, prywatność i koszty
- Zakres programu: cloud vs local models, bezpieczeństwo, koszt.
- Pokrycie w skrypcie NBP:
  - `11:15–12:05 — Cloud-max vs on-prem/local models`
- Ocena: **Pokryte**.

### JSystems 5.3 — Przyszłość: Agentic Workflows & MCP
- Zakres programu: agentic workflows + MCP.
- Pokrycie w skrypcie NBP:
  - `12:05–13:00 — Agentic workflows i MCP`
- Ocena: **Pokryte**.

### JSystems 5.4 — Podsumowanie misji & Lifelong Learning
- Zakres programu: demo finalne, retrospektywa, plan dalszego rozwoju.
- Pokrycie w skrypcie NBP:
  - `09:20–10:05 — Finałowe demo`
  - `13:30–14:20 — Plan wdrożenia po szkoleniu: pierwsze 30 dni`
  - `15:25–16:00 — Zamknięcie kursu: co dalej`
- Ocena: **Pokryte**.

---

## Podsumowanie zgodności (J2)

- Pokrycie modułowe Day 1–Day 5: **kompletne na poziomie struktury i intencji dydaktycznej**.
- Główne miejsce ryzyka (do domknięcia w J3–J6):
  1. Nierówny poziom „dokładnej mowy trenera” między dniami.
  2. Nierówna gęstość inline copy-paste/promptów między blokami.
  3. Potrzeba jawnego odwołania do mapowania modułowego we wstępach dni 2–5.

## Co dalej (dla kolejnych TODO)
- J3–J6: retrofit każdego dnia do pełnego standardu „1 dzień = 1 plik = wszystko pod ręką”.
- W każdym z Day 2–5 dodać sekcję: `Mapowanie do programu JSystems (jawne)` opartą o ten plik.
- J9: audyt użyteczności powinien odwoływać się do tej mapy jako checku zgodności kontraktowej.
