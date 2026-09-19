# Übung: Few-Shot Prompting (Lernen aus Beispielen)

## Ziel der Übung
In dieser Übung erlebst du, wie du Copilot Format, Stil und Entscheidungslogik nicht beschreibst, sondern **vormachst**. Du gibst 2-3 Beispiele (die "Shots") vor, und Copilot überträgt das Muster auf neue Eingaben.

## Lernziele
- Den Unterschied zwischen Zero-Shot, One-Shot und Few-Shot Prompting verstehen
- Gute Beispiele für einen Prompt auswählen und aufbauen
- Ausgabeformate und Tonalität über Beispiele steuern
- Erkennen, wann Beispiele besser wirken als lange Regelbeschreibungen

## Was ist Few-Shot Prompting?
Beim **Few-Shot Prompting** enthält der Prompt mehrere Beispiele für Eingabe und gewünschte Ausgabe. Das Modell erkennt das Muster (Format, Länge, Tonalität, Logik) und wendet es auf die eigentliche Aufgabe an.

| Variante | Beispiele im Prompt | Typischer Einsatz |
|---|---|---|
| Zero-Shot | 0 | Einfache, eindeutige Aufgaben |
| One-Shot | 1 | Format soll grob vorgegeben werden |
| Few-Shot | 2 bis 5 | Muster, Stil oder Klassifikation sollen zuverlässig getroffen werden |

Hinweis: Der Begriff "One-Shot" wird in diesem Kurs auch für einen einzelnen, vollständig formulierten Prompt verwendet (siehe README). Hier ist mit One-Shot gemeint, dass genau **ein Beispiel** im Prompt steht.

## Wann lohnt sich Few-Shot?
- Wenn ein **festes Ausgabeformat** eingehalten werden soll (z. B. Tabellenzeile, Betreffzeile, Kategorie-Label)
- Wenn **Tonalität oder Stil** schwer zu beschreiben, aber leicht zu zeigen sind
- Wenn **Grenzfälle** entschieden werden sollen (z. B. wann ist etwas "Beschwerde" und wann nur "Feedback"?)

## So führst du die Übung durch
1. Öffne Copilot Chat in einer neuen Unterhaltung.
2. Kopiere zuerst den **Zero-Shot Prompt** und notiere dir das Ergebnis.
3. Kopiere danach den **Few-Shot Prompt** in eine neue Unterhaltung.
4. Vergleiche beide Ergebnisse hinsichtlich Format, Konsistenz und Treffsicherheit.
5. Ändere die Beispiele (z. B. anderer Stil, andere Labels) und beobachte, wie sich die Ausgabe mitverändert.

## Schritt 1: Zero-Shot Prompt (Vergleichsbasis)

```text
Ordne die folgende Kundennachricht einer Kategorie zu und formuliere eine einzeilige Zusammenfassung.

Nachricht: "Ihre Rechnung wurde bei mir jetzt schon zum zweiten Mal abgebucht. Ich erwarte eine Erklärung."
```

## Schritt 2: Few-Shot Prompt (copy and use)

```text
Du klassifizierst Kundennachrichten eines Schulungsanbieters.
Gib für jede Nachricht exakt zwei Zeilen aus: "Kategorie:" und "Zusammenfassung:".
Erlaubte Kategorien: Terminproblem, Rechnungsthema, Angebotsanfrage, Beschwerde, Sonstiges.
Die Zusammenfassung hat maximal 12 Wörter und ist sachlich formuliert.

Beispiel 1
Nachricht: "Ich bin am 12.08. leider krank. Kann ich auf einen späteren Termin wechseln?"
Kategorie: Terminproblem
Zusammenfassung: Teilnehmer bittet krankheitsbedingt um Wechsel auf späteren Termin.

Beispiel 2
Nachricht: "Wir planen eine Inhouse-Schulung für 15 Personen. Können Sie mir ein Angebot schicken?"
Kategorie: Angebotsanfrage
Zusammenfassung: Anfrage für Inhouse-Schulung mit 15 Personen, Angebot gewünscht.

Beispiel 3
Nachricht: "Das ist jetzt schon das dritte Mal, dass niemand zurückruft. Das ist inakzeptabel."
Kategorie: Beschwerde
Zusammenfassung: Kunde beklagt wiederholt ausbleibenden Rückruf, Ton verärgert.

Jetzt du:
Nachricht: "Ihre Rechnung wurde bei mir jetzt schon zum zweiten Mal abgebucht. Ich erwarte eine Erklärung."
```

## Erfolgskriterien
- Die Ausgabe besteht aus genau zwei Zeilen im vorgegebenen Format.
- Es wird nur eine der erlaubten Kategorien verwendet.
- Die Zusammenfassung hat höchstens 12 Wörter und wirkt sachlich.
- Im Vergleich zum Zero-Shot Prompt ist das Ergebnis konsistenter und ohne Zusatztext.

## Tipps für gute Beispiele
- **Vielfalt statt Wiederholung:** Beispiele sollten unterschiedliche Fälle abdecken, sonst überträgt Copilot nur ein einziges Muster.
- **Qualität vor Menge:** 2-3 saubere Beispiele wirken besser als 10 unsaubere.
- **Konsistenz:** Alle Beispiele müssen exakt dasselbe Format haben. Abweichungen im Beispiel führen zu Abweichungen in der Ausgabe.
- **Grenzfälle zeigen:** Ein Beispiel für einen schwierigen Fall bringt mehr als ein weiteres eindeutiges.
- **Klare Trennung:** Markiere Beispiele und die eigentliche Aufgabe eindeutig (z. B. "Beispiel 1", "Jetzt du:").
- **Regeln und Beispiele kombinieren:** Kurze Regeln vorab (Format, erlaubte Werte), Beispiele als Beleg.
