# Übung: E-Mail-Analyse und Antwortentwurf im Kundenservice

## Ziel der Übung
In dieser Übung trainierst du einen strukturierten Prompt für die Bearbeitung eingehender Kundenservice-E-Mails.
Die KI analysiert Anliegen, priorisiert, bewertet Risiken und erstellt einen ersten Antwortsatz.

## Lernziele
- E-Mails nach einem klaren 4-Schritte-Modell auswerten
- Signale für Anliegen, Priorität und Risiko zuverlässig erkennen
- Antwortentwürfe regelbasiert und professionell formulieren
- Corporate Wording konsistent anwenden

## Vorbereitung
1. Öffne Copilot Chat.
2. Stelle sicher, dass die Datei Corporate-Wording-Guideline-allgemein.docx als Wissensquelle verfügbar ist.
3. Nutze zusätzlich die Teilnahmebedingungen unter https://www.ihk-akademie-muenchen.de/teilnahmebedingungen/.

## Prompt für die Übung (copy and use)

```text
Sie sind mein Assistent für die Bearbeitung eingehender E-Mails im Kundenservice eines Schulungsanbieters.

Analysieren Sie die folgende E-Mail nach dem 4-Schritte-Prinzip und geben Sie das Ergebnis als Tabelle aus.

SCHRITT 1 – ANLIEGEN (Schwerpunkt):
Benennen Sie das Hauptanliegen in einem Satz. Wählen Sie zusätzlich eine oder mehrere Kategorien.
Nutzen Sie die folgende Signalwort-Referenz zur Orientierung und zitieren Sie zusätzlich die
tatsächlich gefundenen Wörter aus der E-Mail:
- Teilnehmeranfrage: "bin angemeldet", "Bescheinigung", "Zertifikat", "Zugangsdaten", "Unterlagen", "Teilnehmerliste"
- Terminproblem: "verschieben", "wechseln", "anderer Termin", "absagen", "Storno", "verhindert", "krank"
- Rechnungsthema: "Rechnung", "abgebucht", "doppelt", "Erstattung", "Zahlung", "Gutschrift", "Betrag"
- Angebotsanfrage: "Angebot", "Kostenübersicht", "Preis", "Inhouse", "planen", "Konditionen", "unverbindlich"
- Beschwerde: "enttäuscht", "unzufrieden", "schon wieder", "erwarte", "inakzeptabel", "Verantwortlichen sprechen", negativer Ton
- Rückrufwunsch: "rufen Sie mich an", "Rückruf", Telefonnummer ohne Sachkontext, "dringend melden"
Falls die E-Mail mehrere Anliegen enthält, listen Sie jedes Anliegen einzeln.
Falls Kontext fehlt, formulieren Sie eine konkrete Rückfrage.

SCHRITT 2 – PRIORITÄT:
Ordnen Sie ein: Sofort · Heute · Termin · Wiedervorlage · Nur Information.
Begründen Sie die Wahl in einem Satz.

SCHRITT 3 – RISIKO:
Bewerten Sie: Eskalation · Konflikt · Kritischer Kunde · Rechtliches Risiko · Reputationsrisiko · Gering.
Nennen Sie das auslösende Signal. Folgende Risiko-Trigger heben Priorität und Risiko an:
"Anwalt", "Rechtsanwalt", "Frist", "Mahnung", "kündigen", "öffentlich", "im Netzwerk teilen", "seit Jahren Kunde".

SCHRITT 4 – NÄCHSTE AKTION:
Bevor Sie antworten, analysieren Sie die bereitgestellten Bedingungen, um zu verstehen, ob das Anliegen erfüllt werden kann.
Falls nicht, erläutern Sie höflich, warum das Anliegen nicht erfüllt werden kann.
Seien Sie dabei klar und explizit. Erfinden Sie keine möglichen Alternativen, die nicht in den Teilnahmebedingungen der Wissensquelle vorkommen.

WISSENSBASIS:
- Berücksichtigen Sie passende Informationen von der Website https://www.ihk-akademie-muenchen.de/teilnahmebedingungen/
- Wenden Sie das Dokument Corporate-Wording-Guideline-allgemein.docx verbindlich auf Tonalität, Wortwahl und Formulierungen an.
- Falls die Corporate-Wording-Guideline nicht verfügbar oder nicht lesbar ist, stellen Sie zuerst eine klare Rückfrage, bevor Sie den Antwortentwurf erstellen.

AUSGABE:
1. Eine Tabelle mit den Spalten: Schritt | Ergebnis | Begründung/Signal.
2. Darunter ein Vorschlag für den ersten Satz der Antwort-E-Mail in „Sie“-Form, freundlich und lösungsorientiert.

E-MAIL:
[hier die E-Mail einfügen oder auf die markierte E-Mail verweisen]
```

## Mini-Testfall
"Ich bin für den 12.08. angemeldet, bin aber krank und möchte verschieben. Bitte auch klären, ob bereits gezahlte Beträge angerechnet werden."
