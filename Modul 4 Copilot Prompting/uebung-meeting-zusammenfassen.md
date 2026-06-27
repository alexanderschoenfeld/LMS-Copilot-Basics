# Übung: Meeting zusammenfassen — 4 Iterationsschritte

**Modul 4 · Prompting-Grundlagen**  
Das Lizenz Atelier GmbH & Co. KG

---

## Vorbereitung

1. Öffnen Sie Ihr KI-Tool (ChatGPT, Microsoft Copilot, Claude o.ä.)
2. Laden Sie das Beispiel-Transkript hoch oder kopieren Sie es in das Eingabefeld
3. Führen Sie die vier Schritte **nacheinander im selben Gespräch** aus — fangen Sie nicht neu an

> **Wichtig:** Sie müssen das Transkript nur einmal hochladen oder einfügen — beim ersten Prompt. Alle weiteren Prompts bauen auf der bisherigen Konversation auf.

---

## Das Transkript

Laden Sie die Datei **[Meeting_Transkript_Beispiel.docx](Meeting_Transkript_Beispiel.docx)** aus dem Workshop-Ordner hoch — oder kopieren Sie ein eigenes Meeting-Transkript direkt in das Eingabefeld.

---

## ITERATION 01 — Erster Versuch

Kopieren Sie diesen Prompt **als erste Nachricht** in Ihr KI-Tool und laden Sie dabei das Transkript hoch:

```
Fasse mir dieses Meeting zusammen.
```

**Was Sie beobachten werden:** Die Antwort ist generisch — die KI antwortet allgemein, ohne Struktur und ohne Fokus auf das Wesentliche.

---

## ITERATION 02 — Kontext ergänzen

Schicken Sie diesen Prompt als **Folgenachricht** im selben Gespräch:

```
Verbessere deine vorherige Zusammenfassung.
Erstelle eine kompakte, klar strukturierte Zusammenfassung mit maximal 6 Punkten:
Ziel des Meetings
Wichtigste Themen
Wichtigste Entscheidungen
Erwähnte Aufgaben
Offene Punkte
Nächster sinnvoller Schritt
Halte dich kurz und vermeide lange Listen.
```

**Was Sie beobachten werden:** Die KI zieht jetzt konkrete Informationen aus dem Transkript und strukturiert sie entlang Ihrer Vorgaben.

---

## ITERATION 03 — Format anpassen

Schicken Sie diesen Prompt als **nächste Folgenachricht**:

```
Wandle deine vorherige Zusammenfassung in eine priorisierte Thementabelle um.
Nutze genau diese Spalten:
| Priorität | Thema | Kurzbeschreibung in einem Satz | To-Dos | Deadline | Verantwortliche | Offene Punkte |
Regeln:
Maximal 8 Themen.
Priorität als P1, P2 oder P3.
Keine langen Listen.
Wenn keine Deadline genannt wurde, schreibe: nicht genannt.
Wenn keine verantwortliche Person genannt wurde, schreibe: nicht eindeutig genannt.
Nutze nur Informationen aus dem Transkript.
```

**Was Sie beobachten werden:** Das Ergebnis ist jetzt strukturiert, priorisiert und direkt verwendbar — z.B. für einen Status-Report.

---

## ITERATION 04 — Vollständiges Protokoll

Schicken Sie diesen Prompt als **letzten Schritt**:

```
Erstelle jetzt aus dem Transkript und deiner bisherigen Auswertung ein professionelles Meeting-Protokoll.
Das Protokoll soll enthalten:
Meeting-Überblick
  Titel
  Datum, falls erkennbar
  Teilnehmende
  Ziel des Meetings
Management Summary
  Maximal 6 Sätze
  Fokus auf Ergebnis, Relevanz und nächste Schritte
Priorisierte Thementabelle
  Spalten: | Priorität | Thema | Kurzbeschreibung | Entscheidung | To-Dos | Deadline | Verantwortliche |
Aufgabenliste
  Spalten: | Aufgabe | Verantwortliche Person | Deadline | Abhängigkeit | Status |
RACI-Tabelle
  Spalten: | Aufgabe | Responsible | Accountable | Consulted | Informed | Deadline |
Risiken und Klärungsbedarf
  Spalten: | Bereich | Risiko oder Klärungsbedarf | Auswirkung | Empfohlener nächster Schritt |
Offene Fragen
  Nur Punkte, die im Transkript nicht abschließend geklärt wurden.
Nächste Schritte
  Maximal 5 priorisierte Schritte für die nächsten 1 bis 2 Wochen.
Regeln:
Keine endlosen Listen.
Nutze Tabellen, wo immer es sinnvoll ist.
Erfinde keine Namen, Deadlines oder Beschlüsse.
Wenn etwas nicht eindeutig im Transkript steht, schreibe: nicht eindeutig genannt.
Wenn eine Rolle sinnvoll ableitbar ist, kennzeichne sie mit: abgeleitet.
Formuliere sachlich, klar und protokolltauglich.
```

**Was Sie beobachten werden:** Ein vollständiges, sofort verwendbares Protokoll — aus vier gezielten Prompts, ohne das Gespräch neu zu starten.

---

## Reflexion

Nehmen Sie sich kurz Zeit für diese Fragen:

- Welcher Iterationsschritt hat das größte Sprung im Ergebnis gebracht?
- Was hätte die KI ohne Ihre Struktur-Vorgaben in Iteration 02 und 03 gemacht?
- Welche Spalten oder Abschnitte aus Iteration 04 würden Sie für Ihren Arbeitsalltag weglassen oder anpassen?

---

## Eigenes Transkript verwenden

Sie können diese Übung jederzeit mit einem echten Transkript aus Ihrer eigenen Arbeit wiederholen. Teams und Zoom exportieren Transkripte als `.docx` oder `.txt` — einfach hochladen und mit Iteration 01 starten.

---

*Das Lizenz Atelier GmbH & Co. KG · Progress Beats Perfection*
