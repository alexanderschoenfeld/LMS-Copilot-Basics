# One-Shot Prompt: Meeting-Protokoll

**Modul 4 · Prompting-Grundlagen**  
Das Lizenz Atelier GmbH & Co. KG

---

## Warum ein One-Shot Prompt?

In der vorherigen Übung haben Sie dasselbe Ergebnis in vier Iterationsschritten erarbeitet. Das ist der richtige Weg zum Lernen — und oft auch der richtige Weg im Alltag, wenn Sie ein Ergebnis schrittweise formen möchten.

Es gibt aber Situationen, in denen Iteration nicht möglich oder nicht sinnvoll ist:

**Wenn ein Agent die Arbeit übernimmt.**

Agenten — also KI-Systeme, die selbstständig Aufgaben ausführen — können zwar auch mit sich selbst Gespräche führen - das nennt man dann **Reasoning** oder **Thinking**, aber das ist nicht dasselbe wie menschliche Interaktion und in den Reasoning-Modellen (LLM's) schon vorab trainiert. Typischerweise gibt man einem (einzelnen) Agenten einen Prompt, der führt ihn aus, und liefert ein Ergebnis. Kein Nachfragen (ausser vielleicht internes Reasoning), kein Verfeinern, kein zweiter Versuch. Der Prompt muss beim ersten Durchlauf alles enthalten, was die KI braucht: Rolle, Ziel, Format, Regeln, Grenzen und vorallem den perfekten Output. PS: dieser Output wird dann gern an einen anderen Agenten weitergegeben usw., das nennt man **Chaining** oder einen Multi-Agent-Workflow.

Das ist die Kernidee hinter dem One-Shot Prompt: **ein einziger, vollständig ausgearbeiteter Prompt, der in jedem Durchlauf dasselbe, verlässliche Ergebnis liefert** — unabhängig davon, wer ihn ausführt oder wann.

---

## One-Shot vs. Iteration — wann was?

| Situation | Empfehlung |
|---|---|
| Sie erkunden ein Thema, das Ergebnis darf sich entwickeln | Iteration |
| Sie wissen genau, was Sie brauchen, und brauchen es schnell | One-Shot |
| Ein Mensch führt den Prompt aus und kann nachfragen | Iteration möglich |
| Ein Agent führt den Prompt automatisch aus | One-Shot erforderlich |
| Sie wollen dasselbe Ergebnis jedes Mal reproduzieren | One-Shot |
| Sie wollen einen Skill oder eine Automatisierung bauen | One-Shot als Grundlage |

---

## One-Shot Prompts als Vorstufe zum Skill

Ein One-Shot Prompt, der zuverlässig funktioniert, ist im Grunde bereits ein **Skill in Textform**: eine abgeschlossene, wiederverwendbare Fähigkeit mit klarer Eingabe, definiertem Prozess und vorhersehbarer Ausgabe.

Der nächste Schritt wäre, diesen Prompt in einem Agenten-System als Skill zu hinterlegen — dann muss kein Mensch mehr den Prompt kennen oder eintippen. Der Agent ruft den Skill bei Bedarf auf, übergibt das Transkript als Eingabe, und erhält das fertige Protokoll als Ausgabe.

```
Manueller Prompt (Iteration)
        ↓
One-Shot Prompt (deterministisch, reproduzierbar)
        ↓
Skill in einem Agenten (automatisiert, auf Abruf)
```

Die Qualität des One-Shot Prompts bestimmt die Qualität des Skills. Wer einen guten One-Shot Prompt schreiben kann, kann auch einen guten Skill definieren.

---

## Der Prompt

Kopieren Sie den vollständigen Prompt in Ihr KI-Tool. Ersetzen Sie `[TRANSKRIPT EINFÜGEN]` am Ende durch Ihr Transkript — entweder durch direktes Einfügen oder durch Hochladen der Datei und Anpassen des Hinweises.

```
Du bist ein professioneller Meeting-Protokollant und Projektmanager.
Analysiere das folgende Meeting-Transkript und erstelle daraus ein sauberes,
kompaktes und professionelles Meeting-Protokoll.

Ziel:
Das Ergebnis soll nicht nur zusammenfassen, sondern ein nutzbares Arbeitsprotokoll
liefern: mit priorisierten Themen, Entscheidungen, Aufgaben, Verantwortlichen,
Deadlines, Risiken, offenen Fragen und RACI-Zuordnung.

Wichtige Regeln:
- Nutze ausschließlich Informationen aus dem Transkript.
- Erfinde keine Namen, Deadlines, Entscheidungen oder Aufgaben.
- Wenn etwas nicht eindeutig genannt wurde, schreibe: nicht eindeutig genannt.
- Wenn eine Rolle oder Verantwortung sinnvoll aus dem Gespräch ableitbar ist,
  kennzeichne sie mit: abgeleitet.
- Vermeide endlose Listen.
- Fasse ähnliche Punkte sinnvoll zusammen.
- Formuliere sachlich, klar und protokolltauglich.
- Nutze Tabellen, wo Tabellen sinnvoll sind.
- Priorisiere nach geschäftlicher Relevanz, Risiko und Umsetzungsdringlichkeit.

Erstelle das Ergebnis in genau dieser Struktur:

# Meeting-Protokoll

## 1. Meeting-Überblick
| Feld              | Inhalt |
| ----------------- | ------ |
| Titel             |        |
| Datum             |        |
| Teilnehmende      |        |
| Ziel des Meetings |        |
| Zentrale Themen   |        |

## 2. Management Summary
Schreibe maximal 6 Sätze.
Fasse zusammen:
- worum es im Meeting ging,
- welche Ergebnisse erzielt wurden,
- welche Entscheidungen getroffen wurden,
- welche nächsten Schritte wichtig sind.

## 3. Priorisierte Thementabelle
Erstelle maximal 8 Themen.
Nutze genau diese Tabelle:
| Priorität | Thema | Kurzbeschreibung in einem Satz | Entscheidung | To-Dos | Deadline | Verantwortliche | Offene Punkte |
| --------- | ----- | ------------------------------ | ------------ | ------ | -------- | --------------- | ------------- |

Regeln:
- Priorität nur als P1, P2 oder P3.
- P1 = kritisch oder kurzfristig wichtig.
- P2 = wichtig, aber nicht sofort kritisch.
- P3 = relevant, aber nachgelagert.
- Pro Thema nur eine kurze Beschreibung.
- Keine langen Aufzählungen innerhalb der Tabellenzellen.

## 4. Aufgabenliste
Extrahiere alle konkreten Aufgaben aus dem Transkript.
Nutze genau diese Tabelle:
| Aufgabe | Verantwortliche Person | Deadline | Abhängigkeit | Status |
| ------- | ---------------------- | -------- | ------------ | ------ |

Regeln:
- Nur echte Aufgaben aufnehmen.
- Keine allgemeinen Diskussionspunkte als Aufgabe formulieren.
- Status nur verwenden, wenn er aus dem Transkript erkennbar ist, sonst: offen.

## 5. Beschlüsse
Erstelle eine kurze Liste der getroffenen Beschlüsse.
Maximal 10 Beschlüsse.
Formuliere jeden Beschluss als klaren Ergebnissatz.

## 6. RACI-Tabelle
Erstelle eine RACI-Tabelle für die wichtigsten Aufgaben.
Nutze genau diese Tabelle:
| Aufgabe | Responsible | Accountable | Consulted | Informed | Deadline |
| ------- | ----------- | ----------- | --------- | -------- | -------- |

Regeln:
- Responsible = führt die Aufgabe aus.
- Accountable = trägt die Ergebnisverantwortung.
- Consulted = wird fachlich einbezogen.
- Informed = wird informiert.
- Wenn eine Rolle nicht eindeutig genannt wurde: nicht eindeutig genannt.
- Wenn eine Zuordnung abgeleitet wurde: Name / Rolle (abgeleitet).

## 7. Risiken und Klärungsbedarf
Nutze genau diese Tabelle:
| Bereich | Risiko oder Klärungsbedarf | Auswirkung | Empfohlener nächster Schritt |
| ------- | -------------------------- | ---------- | ---------------------------- |

Berücksichtige insbesondere: Datenschutz, Technik, Berechtigungen,
Betrieb, Prozesse, Verantwortlichkeiten.

## 8. Offene Fragen
Liste nur Fragen auf, die im Meeting nicht abschließend geklärt wurden.
Maximal 10 offene Fragen.

## 9. Nächste Schritte
Erstelle maximal 5 priorisierte nächste Schritte für die kommenden 1 bis 2 Wochen.
Nutze genau diese Tabelle:
| Priorität | Nächster Schritt | Verantwortliche Person | Zieltermin |
| --------- | ---------------- | ---------------------- | ---------- |

Hier ist das Transkript:
[TRANSKRIPT EINFÜGEN]
```

---

## Was Sie beobachten werden

Das Ergebnis kommt in einem Durchlauf — keine Nachfragen, keine Zwischenschritte. Die Struktur ist identisch, egal wie unterschiedlich das Transkript ist. Genau das macht diesen Prompt brauchbar als Grundlage für eine Automatisierung.

Vergleichen Sie das Ergebnis mit dem, was Sie in der Iterations-Übung in vier Schritten erarbeitet haben. Der Inhalt sollte vergleichbar sein. Der Unterschied liegt nicht in der Qualität, sondern im Weg dorthin.

---

## Reflexion

- Wo würde dieser Prompt in Ihrem Arbeitsalltag automatisch ausgelöst werden — z.B. nach jedem Teams-Meeting, nach einem bestimmten Stichwort, nach dem Speichern eines Transkripts?
- Welche Regeln im Prompt sind für Sie unverzichtbar — und welche würden Sie für Ihr Team anpassen?
- Was fehlt noch, damit dieser Prompt zu einem vollständigen Skill wird?

---

*Das Lizenz Atelier GmbH & Co. KG · Progress Beats Perfection*
