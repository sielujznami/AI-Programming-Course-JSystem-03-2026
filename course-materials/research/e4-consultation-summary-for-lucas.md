# E4 — Consultation summary for Lucas (decision request)

Data: 2026-03-15
Kontekst: podsumowanie po analizie opcji konceptu aplikacji dla kursu NBP (Phase E1–E3).

## Krótki wniosek
**Rekomendacja główna:** SOC Copilot „Incident Triage”

**Fallback:** Legacy Refactor & Risk Assistant

**Dlaczego rekomendacja główna:**
- Najlepszy fit do realiów bankowych (security + SQL/DB + audytowalność).
- Największa wartość dydaktyczna i zaangażowanie uczestników.
- Bardzo dobre mapowanie na 5 dni i styl Codex-first.
- Pozwala pokazać „jak agent działa w środku” bez przeciążania grupy frameworkami.

**Ryzyka i jak je kontrolować:**
- Scope creep w cyber-temacie → trzymamy się symulowanego datasetu i prostego triage flow.
- AG-UI/CopilotKit jako rdzeń jest za ciężkie → tylko optional 5–10 min demo.

## Wiadomość do wysłania (Teams — primary)
Lucas, po E1–E3 rekomenduję **SOC Copilot Incident Triage** jako główną oś projektu końcowego NBP. 
Fallback: **Legacy Refactor & Risk Assistant** (gdyby grupa potrzebowała prostszego, bardziej legacy-first toru).

Powody: najwyższy fit do kontekstu bankowego (security + SQL), najlepsza wartość edukacyjna i zaangażowanie, oraz mocne dopasowanie do 5 dni i Codex-first.

Czy akceptujesz ten wybór?
- **A)** SOC Copilot (recommended)
- **B)** Legacy Refactor fallback
- **C)** inna opcja (wskaż którą)

Jeśli potwierdzisz dziś, od kolejnego runu spinam F1/F2/F3 pod wybraną ścieżkę.

## Wiadomość fallback (WhatsApp — high-level)
Lucas, szybka decyzja do kursu NBP: rekomenduję projekt **SOC Copilot Incident Triage**, fallback to **Legacy Refactor Assistant**. Daj proszę A/B/C (A=SOC, B=Legacy, C=inna opcja), to od razu spinam kolejne pliki.