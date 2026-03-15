# Trainer Chat Pastes — NBP (Quick Copy)

Cel: jeden plik z gotowymi krótkimi wklejkami na Zoom chat.
Źródła pełne: `prompts/02-module-prompts.md`, `prompts/day-*/day-*-prompt-pack.md`, `materials/references/*.md`.

---

## Day 1

### D1 — Start i kontrakt pracy
```text
Ćwiczenie startowe (5 min):
1) Napisz 1 zdaniem: gdzie AI realnie pomaga Ci dziś w pracy.
2) Napisz 1 ryzyko, którego najbardziej chcesz uniknąć.
Format odpowiedzi: „Pomaga: ... | Ryzyko: ...”
```

### D1 — Quiz diagnostyczny
```text
Quiz (anonimowy): wypełnij proszę formularz z podstaw AI.
Cel: dopasowanie tempa i akcentów kursu (nie ocena uczestników).
Link: <wstaw_link_do_quizu>
```

### D1 — Pomysł -> plan
```text
Przygotuj plan implementacji funkcji <NAZWA_FUNKCJI> dla aplikacji <NAZWA_APP>.
Zwróć: 1) cel biznesowy, 2) kryteria akceptacji, 3) ryzyka, 4) najmniejszy sensowny zakres na dziś.
Bez kodu. Odpowiedź po polsku, punktami.
```

### D1 — Bezpieczny start z agentem
```text
Bezpieczny start z agentem:
- pracujemy na dedykowanym branchu,
- sandbox + approvals są domyślnie włączone,
- zadania dzielimy na małe kroki,
- każdy diff czytamy przed testem/commitem,
- AI daje draft, człowiek podejmuje decyzję.
```

### D1 — WezTerm (opcjonalny komunikat)
```text
WezTerm nie jest obowiązkowy. Pokazujemy go, bo często lepiej znosi TUI/splity/powiadomienia przy dłuższej pracy z agentami. Jeśli Twój obecny terminal działa stabilnie — zostajesz przy nim.
```

---

## Day 2

### D2 — ADR
```text
Stwórz ADR dla decyzji: <TEMAT_DECYZJI> w projekcie <NAZWA_APP>.
Uwzględnij: kontekst, opcje, decyzję, konsekwencje, ryzyka, wpływ na bezpieczeństwo i audyt.
```

### D2 — Model danych
```text
Zaproponuj model danych dla <obszar_domeny>.
Zwróć: encje, relacje, kluczowe atrybuty, 5 reguł walidacji, 3 przykładowe edge-case’y.
```

### D2 — System prompt
```text
Napisz zwięzły system prompt dla agenta codingowego.
Wymuś: małe diffy, brak zmian poza zakresem, jawne założenia, checklistę testów, brak sekretów w kodzie.
```

---

## Day 3

### D3 — Mały slice implementacyjny
```text
Zaimplementuj mały slice: <nazwa_slice>.
Zakres: tylko <pliki/moduły>.
Wynik: diff + krótki opis + lista testów do uruchomienia.
Nie zmieniaj nic poza zakresem.
```

### D3 — Debugging
```text
Pomóż zdebugować błąd.
Objaw: <objaw>
Expected: <oczekiwane>
Actual: <faktyczne>
Logi: <fragment>
Zaproponuj: hipotezy, kroki weryfikacji, minimalną poprawkę.
```

### D3 — Refaktoryzacja
```text
Zrefaktoryzuj <moduł> dla czytelności i utrzymania.
Nie zmieniaj zachowania biznesowego.
Dodaj krótkie uzasadnienie zmian i checklistę regresji.
```

### D3 — Handy.computer (opcjonalny komunikat)
```text
Handy.computer to opcjonalny dodatek: szybciej zbiera notatki głosowe i tłumaczenia PL↔EN, ale core kursu zostaje Codex-first. Jeśli demo instalacji się przeciąga, pokazujemy gotowy przykład i wracamy do głównej ścieżki.
```

---

## Day 4

### D4 — Testy
```text
Wygeneruj testy dla zachowania: <opis_przypadku>.
Bez zmian kodu produkcyjnego, chyba że to konieczne — wtedy opisz dlaczego.
Dodaj przypadki pozytywne, negatywne i edge-case.
```

### D4 — Security audit legacy
```text
Przeprowadź mini-audyt bezpieczeństwa modułu <moduł_legacy>.
Zwróć: top 5 ryzyk, poziom ryzyka, rekomendację naprawy, priorytet wdrożenia.
```

### D4 — CI/CD cloud vs on-prem
```text
Porównaj workflow CI/CD dla:
A) GitHub Actions (cloud)
B) Jenkins + GitHub Enterprise (on-prem)
Dla obu: approvals, security gates, audit trail, koszt utrzymania.
```

---

## Day 5

### D5 — Finalny audit
```text
Zrób finalny przegląd rozwiązania <nazwa_app>.
Oceń: jakość kodu, testowalność, bezpieczeństwo, gotowość do wdrożenia.
Zaproponuj 3 poprawki o najwyższym ROI.
```

### D5 — Adaptacja cloud -> on-prem
```text
Przygotuj plan adaptacji workflow z cloud do on-prem/local models.
Uwzględnij: model hosting, sekrety, logowanie, approvals, ograniczenia sieciowe.
```

### D5 — Plan 30 dni
```text
Przygotuj plan 30 dni wdrożenia AI workflow w zespole developerskim.
Podziel na tygodnie, dodaj KPI, ryzyka i szybkie wygrane.
```

---

## Notatka trenerska
- Ten plik ma być szybki (copy/paste).
- Dłuższe wersje i warianty: `prompts/02-module-prompts.md` oraz packi dzienne w `prompts/day-*/`.
- Jeśli uczestnicy pracują w środowisku regulowanym: przypominaj o zasadzie „bez danych wrażliwych w promptach”.
