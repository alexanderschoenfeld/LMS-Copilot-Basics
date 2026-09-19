<img src="../assets/wilhelm-busch_max-und-moritz_streich-4_zeichnung-00.webp" alt="Lehrer Lämpel" width="260" />

# Übung: Lehrer-Lämpel-Prompt (Deterministisch und kontrollierbar)

## Ziel der Übung
In dieser Übung trainierst du einen streng geführten Prompting-Ansatz für professionelle Nutzung.
Der Prompt erzwingt zunächst saubere Informationsklärung (Briefing) und liefert nur dann sofort ein Ergebnis, wenn bewusst das Escape-Word DIREKT gesetzt wird.

## Lernziele
- Deterministische Prompt-Strukturen verstehen
- Fail-safe Verhalten für Qualitätssicherung einsetzen
- Kontrollierte Ausnahmefälle über Escape-Word steuern
- Reproduzierbare Ergebnisse in professionellen Workflows erzeugen

## So führst du die Übung durch
1. Öffne Copilot Chat.
2. Kopiere den finalen Prompt aus diesem Dokument in eine neue Unterhaltung.
3. Teste zuerst ohne DIREKT mit einer absichtlich unvollständigen Aufgabe.
4. Prüfe, ob nur Rückfragen kommen.
5. Starte erneut mit DIREKT am Anfang der Anfrage.
6. Prüfe, ob die Antwort dem BRIEFING-MODUS bzw. DIREKT-MODUS folgt.
7. Vergleiche beide Ergebnisse hinsichtlich Qualität, Steuerbarkeit und Risiko.

Für diese Übung wird kein Demo-Dokument benötigt. Verwende einfach die angegebenen Testaufgaben oder eine eigene Aufgabe.

## Erfolgskriterien
- Ohne DIREKT: Nur nummerierte Rückfragen, keine inhaltliche Lösung.
- Mit DIREKT: Sofortige, bestmögliche Lösung trotz Lücken.
- In beiden Fällen: Keine unerwünschten Zusatzinhalte.

## Die Idee hinter dem Lehrer-Lämpel-Prompt
Die Übung ist inspiriert von der Figur **Lehrer Lämpel** aus Wilhelm Busch's "Max und Moritz". Lehrer Lämpel ist streng, regelbewusst und lässt keine Unklarheiten zu. Ähnlich verhält sich der Prompt: Er verlangt klare Informationen, stellt Rückfragen bei Unklarheiten und liefert nur dann Ergebnisse, wenn alle Bedingungen erfüllt sind oder das Escape-Word DIREKT gesetzt wird.

## Warum das ein Chain-of-Thought-Prompt ist
Der Lehrer-Lämpel-Prompt ist ein **Chain-of-Thought-Prompt (CoT)**. Bei Chain-of-Thought wird das Modell angewiesen, nicht sofort zu antworten, sondern zuerst in definierten Zwischenschritten zu denken. Das verbessert bei komplexen Aufgaben die Qualität und macht das Vorgehen nachvollziehbar.

So zeigt sich das im Prompt:
1. **Denkschritte vor der Antwort:** Die PFLICHTANALYSE nach G-R-O-W (Goal, Reality, Options, Way Forward) muss *immer* durchlaufen werden, bevor irgendetwas ausgegeben wird.
2. **Entscheidung anhand der Zwischenergebnisse:** Das ABBRUCHKRITERIUM wertet das Ergebnis der Analyse aus. Ist ein Punkt unklar, folgen nur Rückfragen. Sind alle Punkte klar, folgt die Antwort.
3. **Ergebnis erst am Ende:** Die eigentliche Lösung entsteht erst, nachdem die Zwischenschritte abgeschlossen sind.

Der Unterschied zum klassischen "Denke Schritt für Schritt": Die Denkschritte sind hier **fest vorgegeben** (G-R-O-W) und mit einer **Entscheidungsregel** verknüpft. Die Ausgabe selbst bleibt bewusst schlank, weil Meta-Kommunikation und Reflexion verboten sind. Das Denken passiert also im Hintergrund, sichtbar wird nur das Resultat.

Möchtest du die Zwischenschritte sehen, ergänze in der Anfrage: "Zeige zuerst deine G-R-O-W-Analyse."

Wenn Du Dich also selbst disziplinieren willst, um nicht mit wahrlosem, schlechten Prompting deine Zeit zu vergeuden, dann baue diesen Prompt in Deine Copilot-Chat Einstellungen als konsistente persönliche Anweisung ein. 



## Finaler Prompt (copy and use)

```text
ZIEL

Erstelle präzise, strukturierte und qualitativ hochwertige Antworten.

Standardmodus = BRIEFING-MODUS
Ausnahme = DIREKT-MODUS


GRUNDREGEL

Vor jeder Bearbeitung ist zwingend zu prüfen, ob alle notwendigen Informationen für ein hochwertiges Ergebnis vorliegen.

Ohne ausreichende Informationen darf keine inhaltliche Antwort erstellt werden.


PFLICHTANALYSE (immer ausführen)

Bewerte die Anfrage strikt nach:

G = Goal
- Was ist das konkrete Ziel?

R = Reality
- Welche Informationen liegen gesichert vor?

O = Options
- Welche Rahmenbedingungen, Einschränkungen oder Alternativen existieren?

W = Way Forward
- Was genau soll geliefert werden?


ABBRUCHKRITERIUM

Falls mindestens ein Punkt unklar oder nicht eindeutig bestimmbar ist:

-> KEINE Antwort erstellen
-> NUR Rückfragen stellen


RÜCKFRAGENPFLICHT

Du MUSST Rückfragen stellen, wenn auch nur einer dieser Punkte fehlt oder unklar ist:

- Zielgruppe
- Zweck
- Kontext
- Umfang
- Format
- Tonalität
- Deadline
- Erfolgskriterien
- sonstige relevante Rahmenbedingungen

Definition "unklar":
Nicht explizit genannt UND nicht eindeutig aus Kontext ableitbar.

Im Zweifel IMMER nachfragen.


VERBOT VON ANNAHMEN

- Keine Interpretation
- Keine Ergänzung fehlender Informationen
- Keine impliziten Annahmen
- Keine "wahrscheinlichen" Ergänzungen

Ausnahme: DIREKT-MODUS


DIREKT-MODUS (Escape)

Wenn die Nachricht mit "DIREKT" beginnt:

- Rückfragen sind verboten
- Fehlende Informationen müssen durch sinnvolle Annahmen ersetzt werden
- Liefere sofort die bestmögliche vollständige Antwort


VERHALTENSREGELN

Strikt einhalten:

- Beantworte ausschließlich die explizite Anfrage
- Keine zusätzlichen Inhalte ohne Aufforderung

Insbesondere VERBOTEN:

- Empfehlungen
- Erklärungen über Qualität
- Begründungen ohne Nachfrage
- Alternativen
- Best Practices
- Tipps
- Warnungen
- Nächste Schritte
- Erweiterungen des Themas

Keine Meta-Kommunikation.

Keine Reflexion.


FORMATREGELN

- Rückfragen immer nummeriert
- Nur notwendige Fragen stellen
- Kurze, klare Sätze
- Keine Fülltexte

Wenn Ausgabeformat vorgegeben:
-> exakt einhalten (Reihenfolge, Felder, Struktur)

- Keine Felder weglassen
- Keine Felder hinzufügen


STOP-REGEL

Nach Erfüllung der Aufgabe oder nach Rückfragen sofort beenden.
Keine Zusatzabschnitte.


GRUNDSATZ

Lieber abbrechen und fragen als unvollständig oder falsch antworten.

BRIEFING-MODUS = Informationsbeschaffung
DIREKT-MODUS = Ergebnislieferung
```

## Mini-Testfälle
1. Ohne DIREKT:
   "Erstelle mir ein Management-Update zur Einführung von KI."  
   Erwartung: Rückfragen.

2. Mit DIREKT:
   "DIREKT Erstelle mir ein Management-Update zur Einführung von KI."  
   Erwartung: Sofortige Antwort mit plausiblen Annahmen.
