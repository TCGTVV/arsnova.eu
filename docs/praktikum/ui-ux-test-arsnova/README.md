<!-- markdownlint-disable MD013 -->

# UI/UX-Test arsnova.eu — Material- & Vorlagenpaket

Komplettes Arbeitsmaterial für den Remote-UI/UX-Test mit **Thinking Aloud** und **VisAWI** laut
[Arbeitsauftrag](../ARBEITSAUFTRAG-UI-UX-THINKING-ALOUD-VISAWI.md).

- **Zielsystem:** Produktionsserver <https://arsnova.eu>
- **Methode:** Remote (Teams/Zoom), zwei getrennte Einzelsitzungen, **Audio-only** nach Einwilligung
- **Preset:** „Spielerisch" in beiden Sitzungen
- **Deadline:** **24. Juni 2026**

## Datei-Index

| Phase        | Datei                                                              | Zweck                                                                      |
| ------------ | ------------------------------------------------------------------ | -------------------------------------------------------------------------- |
| **Tracking** | [HANDOVER.md](HANDOVER.md)                                         | **Aktueller Status & exakte nächste Schritte — hier einsteigen**           |
| Vorbereitung | [einwilligung-datenschutz.md](einwilligung-datenschutz.md)         | Einwilligungs- und Datenschutztext, mündliche Bestätigung                  |
| Vorbereitung | [pre-flight-checkliste.md](pre-flight-checkliste.md)               | Technik-, Termin- und Produktkonfiguration vor jeder Sitzung               |
| Durchführung | [moderationsskript.md](moderationsskript.md)                       | Roter Faden je Sitzung: Begrüßung, Warm-up, neutrale Moderation, Abschluss |
| Durchführung | [aufgabenkarte-quizmaster.md](aufgabenkarte-quizmaster.md)         | Szenario + Aufgaben (Testperson) + Beobachtungsschwerpunkte (Testleitung)  |
| Durchführung | [aufgabenkarte-quizteilnehmer.md](aufgabenkarte-quizteilnehmer.md) | Szenario + Aufgaben (Testperson) + Beobachtungsschwerpunkte (Testleitung)  |
| Durchführung | [protokollvorlage.md](protokollvorlage.md)                         | Beobachtungsprotokoll, je Sitzung kopieren                                 |
| Auswertung   | [vorlage_transkript.md](vorlage_transkript.md)                     | Transkript-Gerüst (Abschnitt 12)                                           |
| Auswertung   | [vorlage_ui-ux-issues-moscow.md](vorlage_ui-ux-issues-moscow.md)   | MoSCoW-Issue-Liste (Abschnitt 13)                                          |
| Abgabe       | [email-vorlage.md](email-vorlage.md)                               | E-Mail an den Kursleiter (Abschnitt 14)                                    |

## Ablauf in Kurzform

1. **Pro Sitzung vorab:** Pre-Flight-Checkliste abarbeiten (Technik + Produktkonfiguration).
2. **Sitzungsstart:** Begrüßung → Einwilligung einholen → Aufnahme starten → mündliche Bestätigung der Einwilligung.
3. **Warm-up** zum lauten Denken, dann rollenbezogene Aufgaben (Aufgabenkarte). Testleitung moderiert neutral, greift nicht ein.
4. **Abschluss:** Abschlussfrage, dann VisAWI-Fragebogen eigenständig ausfüllen lassen.
5. **Nach der Sitzung:** Audio → KI-Transkript (Vorlage), daraus UI/UX-Issues nach MoSCoW (Vorlage).
6. **Abgabe:** vier Markdown-Dateien per E-Mail an den Kursleiter bis 24.06.2026.

## Pflicht-Deliverables (mind. 4 Dateien)

- [ ] `YYYY-MM-DD_quizmaster_transkript.md`
- [ ] `YYYY-MM-DD_quizmaster_ui-ux-issues-moscow.md`
- [ ] `YYYY-MM-DD_quizteilnehmer_transkript.md`
- [ ] `YYYY-MM-DD_quizteilnehmer_ui-ux-issues-moscow.md`

> `YYYY-MM-DD` = jeweiliges Sitzungsdatum. Die Auswertungs-Vorlagen kopieren und exakt nach diesem Schema umbenennen.

## Verifizierte Produkt-Facts (gegen den arsnova.eu-Code geprüft, Stand 2026-06-21)

Damit in den Sitzungen keine UI-Realität von den Auftragsvorgaben abweicht:

- **Preset „Spielerisch" ist Default beim Erstbesuch.** Es gibt nur zwei Presets („Seriös"/„Spielerisch"); ein abweichend gespeicherter Stil bliebe erhalten, daher vor Testbeginn prüfen und ggf. zurückstellen.
- **Pseudonym-Sets im Dropdown „Altersgruppe für Pseudonyme":** Nobelpreisträger, **Kindergarten** (Tier-Emojis), Grundschule, Mittelstufe, Oberstufe. Für den Test gezielt **Kindergarten** wählen.
- **Quizmaster-Session:** Das gamifizierte Quiz (2 Teams, Kindergarten-Pseudonyme) wird von der Testperson **selbst angelegt**.
- **Quizteilnehmer-Session:** Das Demo-Quiz **„Praxis-Showcase: Team-Quiz"** existiert, hat **genau 9 Fragen** und ist **bereits gamifiziert** (2 Teams, `nicknameTheme = Kindergarten`). Es wird beim ersten Start ohne vorherige Nutzung in der Quizsammlung angeboten.

## Hinweise

- Materialordner ist eigenständig; Pfad/Commit nach Bedarf anpassen. Reale Transkripte/Audios enthalten personenbezogene Daten → **anonymisieren** und nicht versehentlich committen.
- Alle Vorlagen sind bewusst frei von UI-Schritt-für-Schritt-Anleitungen für die Testperson (realistische Aufgaben statt Bedienhinweise).
