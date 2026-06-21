# CLAUDE.md — temporäre Session-Übergabe (nicht committen)

> **Zweck:** Übergabe-Notiz zwischen Modell-Wechsel innerhalb derselben Praktikumsaufgabe.
> Diese Datei wird **nicht committet** und nach dem Agenten-Wechsel wieder gelöscht.

## Modell-Switch

- Bisheriges Modell dieser Session: **Claude Opus 4.7** (`claude-opus-4-7`)
- Neues Modell ab jetzt: **Claude Opus 4.8** (`claude-opus-4-8`)
- Grund: Nutzer möchte mit aktuellerem Modell weiterarbeiten.

## User-Kontext (aus Auto-Memory)

- Sprache: **Deutsch**. Antworte auf Deutsch.
- E-Mail: `elreydelorbe@pm.me`
- Heutiges Datum: **2026-06-21**
- Bestehende Feedback-Memory: _„Erst prüfen, dann anleiten"_ — keine Anleitungen geben, ohne Berechtigungen/Voraussetzungen vorher zu klären.
- Auto-Mode aktiv: Bias zu Handeln statt Rückfragen, aber bei echten Entscheidungen (Methodik, Branch-Naming, destruktive Aktionen) nachfragen.

## Repo-Setup

- Pfad: `/Users/leopoldgrund/projects/arsnova.eu`
- Remotes: `origin` = `github.com/TCGTVV/arsnova.eu` (Fork des Users), `upstream` = `github.com/kqc-real/arsnova.eu` (Original).
- Aktueller Branch: **`task/ui-ux-thinking-aloud-visawi`** (frisch, leer; vom aktualisierten `main` abgezweigt).
- Vorgängerbranch `feat/numeric-estimate-1-2d` wurde lokal **und** auf der Fork (origin) gelöscht — abgeschlossen mit PR #24 in upstream.
- `main` wurde frisch via `git fetch upstream && git merge --ff-only upstream/main` aktualisiert (79 Commits) und an `origin/main` gepusht.
- Working tree clean.

## Was in dieser Session bereits passiert ist

1. **Serena-MCP-Server** (semantische Code-Tools) ist verbunden und funktionsfähig getestet (`mcp__serena__find_symbol`, `mcp__serena__list_memories` etc.). Bei Code-Aufgaben Serena bevorzugen statt Read/Grep/Edit — siehe `mcp__serena__initial_instructions`.
2. Fork wurde mit Upstream synchronisiert (s. o.).
3. Alter Feature-Branch entsorgt, neuer Aufgaben-Branch angelegt.
4. **Arbeitsauftrag gelesen:** [docs/praktikum/ARBEITSAUFTRAG-UI-UX-THINKING-ALOUD-VISAWI.md](docs/praktikum/ARBEITSAUFTRAG-UI-UX-THINKING-ALOUD-VISAWI.md)
5. Relevante Serena-Memories gelesen: `core`, `frontend/core`, `session/lifecycle`, `conventions`, `tech_stack`. **Nicht** gelesen, evtl. später relevant: `frontend/i18n-ui`, `frontend/routing-components`, `landing/core`, `quality/dod`, `quality/workflow`, `modules/frontend`, `modules/product`.

## Der Auftrag in Kürze

Praktikums-Hausaufgabe (Case Study) für arsnova.eu — **kein Code-Task, sondern User-Research**:

- **Methode:** Remote-Thinking-Aloud + VisAWI-Befragung (Pilot-Test mit je 1 Testperson pro Rolle).
- **2 getrennte Remote-Sitzungen** (Teams/Zoom), jeweils 30–60 min, **Audio-only-Aufzeichnung** nur nach Einwilligung.
- **Rolle 1: Quizmaster** im Desktop-Browser — erstellt gamifiziertes Quiz mit 2 Teams, Pseudonym-Set „Kindergarten (Tier-Emojis)", einer Single-Choice- und einer Multiple-Choice-Frage (je 4 Optionen), mind. 2 Markdown-Features. Testleitung tritt im Smartphone als Teilnehmer bei.
- **Rolle 2: Quizteilnehmer/in** im Smartphone-Browser — nimmt am Demo-Quiz „Praxis-Showcase: Team-Quiz" (9 Fragen) teil, das die Testleitung im Desktop hostet.
- **Zielsystem:** Produktionsserver `https://arsnova.eu` (nicht lokal!) — kein Dev-Setup nötig.
- **Preset:** „Spielerisch" in beiden Sitzungen.
- **Deliverables (mind. 4 Markdown-Dateien):** je Rolle ein Transkript + eine MoSCoW-priorisierte UI/UX-Issue-Liste. Versand per E-Mail an Kursleiter.
- **Dateinamen:** `YYYY-MM-DD_rolle_transkript.md`, `YYYY-MM-DD_rolle_ui-ux-issues-moscow.md`.
- **DEADLINE: 24. Juni 2026** — nur noch **3 Tage** ab heute (2026-06-21).

Detailstruktur, Aufgabenlisten und Beobachtungsschwerpunkte sind im Auftrags-Markdown ausgeschrieben (Abschnitte 8–13).

## Wichtige Fakten aus den gelesenen Memories

- arsnova.eu ist Angular 21 + tRPC + Prisma/PostgreSQL + Redis Monorepo (npm workspaces). Frontend liefert 5 Locales (de Quelle, en/fr/es/it).
- Quiz-Editor hat zentralen Save-Flow (siehe `mem:frontend/quiz-editor-save-flow`, falls Quiz-Erstellung im Detail relevant wird).
- Markdown-Editor unterstützt Toolbar mit Überschrift, Fett/Kursiv, Liste, Zitat, Inline-Code, Formel, Link, Bild, Codeblock, Block-Formel, Kurzhilfe, Vorschau.
- Session-Lifecycle: `LOBBY` → `QUESTION_OPEN` (mit reading phase) → `ACTIVE` → `RESULTS` → `FINISHED`. Host steuert Phasenwechsel.
- Pseudonym-Sets und Presets sind im Frontend definiert — bei Bedarf via Serena (`find_symbol` / `get_symbols_overview` auf `apps/frontend/src/app/features/quiz/...`) verifizieren.

## Was als nächstes zu tun ist

**Letzte User-Aussage:** „bevor wir anfangen aber noch eine frage: auf welchem modell läufst du?" → Modell-Antwort gegeben, dann Aufforderung zum CLAUDE.md-Write (das ist diese Datei).

**Offene Klärungsfragen** (Auto-Mode-Frage wurde vom User abgebrochen, weil zuerst die Übergabe erstellt werden sollte). Nach Modell-Switch erneut stellen oder direkt aufgreifen:

1. **Heutiger Fokus** — eine dieser vier Richtungen (in absteigender Sinnhaftigkeit, falls die Auswahl frei wäre):
   - (A) **Vorbereitungs-Pakete bauen:** Einwilligungsformular, Moderationsskript (Begrüßung/Warm-up/Abschluss), Protokollvorlage, Aufgabenkarten je Rolle, Pre-Flight-Checkliste. Ablage z. B. unter `docs/praktikum/visawi-thinking-aloud/`.
   - (B) **Produkt-Facts gegenprüfen** via Serena: Existiert das Demo-Quiz „Praxis-Showcase: Team-Quiz" mit genau 9 Fragen? Heißt das Pseudonym-Set wirklich „Kindergarten (Tier-Emojis)"? Ist „Spielerisch" beim Erstbesuch Default? — damit der Nutzer nicht in der Sitzung von UI-Realität überrascht wird.
   - (C) **Auswertungs-Templates bauen:** Transkript-Template + MoSCoW-Issue-Liste-Template (Auftrag Abschnitt 12 & 13), korrektes Dateinamensschema.
   - (D) **Spezifische Hilfe** für eine konkrete bevorstehende Sitzung.

2. **Rekrutierungs-Status:** Sind die beiden Testpersonen schon zugesagt, Termine fix? Bei nur 3 Tagen Restlaufzeit kritisch — ggf. Rekrutierungstext mit aufnehmen.

## Verhaltens-Hinweise für den nächsten Agenten

- **Deutsch** antworten, knapp, ohne Emojis (außer User fragt explizit).
- **Auto-Mode aktiv:** Lieber handeln und melden statt unnötig zurückfragen — außer bei echten Entscheidungen.
- **Serena bevorzugen** für jegliche Code-Exploration (`get_symbols_overview`, `find_symbol`, `find_referencing_symbols`) statt Read/Grep/Edit. Auch Memories über `mcp__serena__read_memory` weiterlesen, wenn relevant.
- **Nichts ungefragt committen.** User entscheidet committen, pushen, PR-Erstellung.
- **Diese Datei (CLAUDE.md) ist temporär** und wird vom User entfernt; nicht ins Repo committen, nicht im PR-Body erwähnen.
- Bei UI/Copy-Änderungen in der App wären alle 5 Locales mitzupflegen — für diesen Auftrag jedoch unwahrscheinlich relevant (Pilot-Test, keine Code-Änderungen).
- Wenn der Nutzer eine "Schedule"-Aktion erwähnt oder es eine fixe Folge-Verpflichtung gibt: hier liegt die Deadline 2026-06-24, aber das ist sein Termin, nicht meiner — keine ungefragte `/schedule`-Offer.

## Quick-Reference Pfade

- Auftrag: `docs/praktikum/ARBEITSAUFTRAG-UI-UX-THINKING-ALOUD-VISAWI.md`
- Demo-Quiz-Daten (Showcase): `apps/frontend/src/assets/demo/quiz-demo-showcase.{de,en,es,fr,it}.json`
- Quiz-Edit-Komponente: `apps/frontend/src/app/features/quiz/quiz-edit/`
- Session-Komponenten: `apps/frontend/src/app/features/session/`
- Join-Komponente (Teilnehmer-Beitritt): `apps/frontend/src/app/features/join/`
- Home-Komponente (Startseite/Preset): `apps/frontend/src/app/features/home/`
- Theme/Preset-Service: `apps/frontend/src/app/core/theme-preset.service.ts`
