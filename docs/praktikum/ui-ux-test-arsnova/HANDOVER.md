<!-- markdownlint-disable MD013 -->

# HANDOVER — Status & nächste Schritte: UI/UX-Test arsnova.eu

> Persönlicher Tracker für die Praktikumsaufgabe. Hier startest du, wenn du wieder einsteigst.
> Stand: **2026-06-21**. **Deadline: 24.06.2026.**

## Status auf einen Blick

|                             |                                                                                                                   |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Aufgabe                     | Remote-UI/UX-Test (Thinking Aloud + VisAWI), 2 Rollen, 2 Sitzungen                                                |
| Zielsystem                  | <https://arsnova.eu> (Produktion), Preset „Spielerisch"                                                           |
| **Material/Vorlagen**       | ✅ **fertig** (alle Dateien in diesem Ordner)                                                                     |
| **Produkt-Check**           | ✅ **erledigt** (Demo-Quiz, 9 Fragen, 2 Teams, Kindergarten-Pseudonyme, „Spielerisch"-Default gegen Code geprüft) |
| **Testpersonen rekrutiert** | ❓ offen — **kritischer Pfad**                                                                                    |
| **Sitzungen durchgeführt**  | ⬜ 0 von 2                                                                                                        |
| **Deliverables abgegeben**  | ⬜ 0 von 4 Dateien                                                                                                |
| Restzeit                    | **3 Tage**                                                                                                        |

## Was bereits erledigt ist

- Komplettes Material- und Vorlagenpaket erstellt (siehe [README.md](README.md)): Einwilligung, Pre-Flight-Checkliste, Moderationsskript, 2 Aufgabenkarten, Protokollvorlage, Transkript-Vorlage, MoSCoW-Issue-Vorlage, E-Mail-Vorlage.
- Produkt-Realität gegen den arsnova.eu-Code verifiziert → in keiner Sitzung sollten dich die Vorgaben überraschen.

## ⚠️ JETZT zuerst (kritischer Pfad: Rekrutierung)

Ohne Testpersonen läuft nichts, und es bleiben nur 3 Tage. **Heute erledigen:**

- [ ] **2 Testpersonen anfragen** (1× Quizmaster-Typ, 1× Teilnehmer-Typ). Anforderung: nicht an der UI-Entwicklung beteiligt, bereit zu lautem Denken + Audioaufnahme + KI-Transkription, ~45–60 min Zeit. Einladungstext-Vorschlag siehe unten.
- [ ] **Je einen Remote-Termin** (Teams/Zoom) für **22.06.** und/oder **23.06.** fixieren.
- [ ] **Technik vorbereiten:** Teams/Zoom mit funktionierender **Audioaufnahme**, Desktop-Browser (Host) + Smartphone-Browser (Teilnahme) bereitlegen, zweiter Zugang für deine Gegenrolle.
- [ ] **Smoke-Test:** <https://arsnova.eu> auf allen Geräten öffnen, ggf. Update-Hinweis annehmen, prüfen dass Preset „Spielerisch" aktiv ist und das Demo-Quiz „Praxis-Showcase: Team-Quiz" in der Sammlung auftaucht.

## Schritt-für-Schritt: pro Sitzung

> Detailtexte stehen in den verlinkten Dateien — hier nur die Reihenfolge.

1. [ ] **Pre-Flight-Checkliste** für die jeweilige Rolle abarbeiten → [pre-flight-checkliste.md](pre-flight-checkliste.md)
2. [ ] Begrüßung + Einwilligung → [einwilligung-datenschutz.md](einwilligung-datenschutz.md), dann **Audio starten** + mündliche Bestätigung
3. [ ] Technikcheck + Warm-up + Aufgaben nach **Moderationsskript** → [moderationsskript.md](moderationsskript.md)
4. [ ] Passende **Aufgabenkarte** verwenden (Teil A vorlesen/teilen, Teil B nur für dich):
       [Quizmaster](aufgabenkarte-quizmaster.md) · [Quizteilnehmer/in](aufgabenkarte-quizteilnehmer.md)
5. [ ] Beobachtungen live ins **Protokoll** (Kopie je Sitzung) → [protokollvorlage.md](protokollvorlage.md)
6. [ ] Abschlussfrage, dann **VisAWI** ausfüllen lassen → <https://esurvey.uid.com/survey/#468e011e-6cc4-4ff4-8e1a-69895523e19e>
7. [ ] **Audiodatei sichern** nach Schema `YYYY-MM-DD_rolle_testperson-audio.mp3`

## Schritt-für-Schritt: Auswertung (nach jeder Sitzung)

1. [ ] Audio + [vorlage_transkript.md](vorlage_transkript.md) an ein aktuelles LLM/Transkriptionssystem → Transkript erzeugen
2. [ ] Transkript auf **Lesbarkeit + Anonymisierung** prüfen, umbenennen zu `YYYY-MM-DD_rolle_transkript.md`
3. [ ] Aus Transkript + Protokoll die **UI/UX-Issues** ableiten → [vorlage_ui-ux-issues-moscow.md](vorlage_ui-ux-issues-moscow.md), umbenennen zu `YYYY-MM-DD_rolle_ui-ux-issues-moscow.md`
4. [ ] Jedes Issue: Rolle, Beobachtung/Zitat, Ursache, Auswirkung, **MoSCoW-Priorität**, Verbesserungsvorschlag
       → _Diesen Schritt kann Claude für dich übernehmen, wenn du Transkript/Protokoll lieferst._

## Abgabe (Schluss)

- [ ] Vier Dateien vollständig + anonymisiert (siehe Checkliste unten)
- [ ] E-Mail an Kursleiter nach [email-vorlage.md](email-vorlage.md) senden — **bis spätestens 24.06.2026**

## Zeitplan-Vorschlag (anpassen nach Verfügbarkeit der Testpersonen)

| Datum                 | Vorhaben                                                                        |
| --------------------- | ------------------------------------------------------------------------------- |
| **21.06.** (heute)    | Rekrutierung, Termine fixieren, Technik + Smoke-Test                            |
| **22.06.**            | Sitzung(en) durchführen (idealerweise beide; sonst eine), Audio sichern, VisAWI |
| **23.06.**            | restliche Sitzung + Auswertung beider Sitzungen (Transkripte + Issue-Listen)    |
| **24.06.** (Deadline) | Finalisieren, anonymisieren, **E-Mail-Abgabe vormittags** (Puffer)              |

> Engpass-Fallback: Beide Sitzungen am selben Tag mit Pause dazwischen sind möglich (je 30–60 min + VisAWI).

## Pflicht-Deliverables

- [ ] `YYYY-MM-DD_quizmaster_transkript.md`
- [ ] `YYYY-MM-DD_quizmaster_ui-ux-issues-moscow.md`
- [ ] `YYYY-MM-DD_quizteilnehmer_transkript.md`
- [ ] `YYYY-MM-DD_quizteilnehmer_ui-ux-issues-moscow.md`

## Wer macht was

| Du (Testleitung)                               | Claude                                                            |
| ---------------------------------------------- | ----------------------------------------------------------------- |
| Testpersonen rekrutieren, Termine, Einladungen | Material/Vorlagen erstellt ✅                                     |
| Sitzungen moderieren, Audio aufnehmen          | Transkripte aus Audio/Roh-Text in Vorlage gießen (Anonymisierung) |
| VisAWI ausfüllen lassen                        | UI/UX-Issues nach MoSCoW ableiten + formulieren                   |
| E-Mail final versenden                         | Abgabe-Dateien gegen Auftragsvorgaben prüfen                      |

## Einladungstext-Vorschlag (zum Anpassen)

```text
Hallo [Name],

für eine Lehrveranstaltung mache ich einen kurzen UI/UX-Test der Web-App arsnova.eu und suche
eine Testperson für die Rolle [Quizmaster / Quizteilnehmer/in]. Es dauert ca. 45–60 Minuten,
läuft remote per [Teams/Zoom], und du nutzt einfach die App, während du laut aussprichst, was
dir auffällt. Getestet wird die App, nicht du. Aufgezeichnet wird nur Audio (mit deiner
Zustimmung), das anschließend KI-gestützt transkribiert und anonymisiert ausgewertet wird.

Hättest du am [22.06.] oder [23.06.] ca. eine Stunde Zeit?

Danke dir und viele Grüße
[Dein Name]
```

## Offene Entscheidungen / Risiken

- **Rekrutierung ist das Hauptrisiko** bei 3 Tagen Restzeit — heute starten.
- Ablageort dieser Materialien: aktuell `docs/praktikum/ui-ux-test-arsnova/` (untracked, **nicht committet**). Reale Transkripte/Audios enthalten personenbezogene Daten → anonymisieren und bewusst entscheiden, ob/wohin sie gehören (ggf. außerhalb des Repos).
- Reihenfolge der Rollen ist frei wählbar; beide Sitzungen sind unabhängig.
