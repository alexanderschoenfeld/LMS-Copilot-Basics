# LMS Copilot Basics - Öffentliche Ausschnitte

Dieses Repository zeigt öffentlich verfügbare Auszüge aus dem Learning Management System **Copilot Basics**.

Das komplette LMS **Copilot Basics** ist eine umfassende Schulung mit **14 Modulen** und **88 Lernsessions**. In diesem Repository werden bewusst nur einzelne Ausschnitte bereitgestellt, um Einblicke in Aufbau, Methodik und Prompting-Praxis zu geben.

## Modul 4: Copilot Prompting

In [Modul 4 Copilot Prompting](Modul%204%20Copilot%20Prompting/) findest du mehrere Prompting-Übungen sowie einen Prompt für den ["Prompt Coach"](Modul%204%20Copilot%20Prompting/prompt_coach.md), inspiriert vom gleichnamigen Microsoft prebuilt Copilot Agent.

Die [Copilot-Chat-Anweisung](Modul%204%20Copilot%20Prompting/copilot_chat_anweisung.md) ergänzt diese Übungen um eine persönliche Systemanweisung für alle Unterhaltungen. Sie sorgt für konsistente, lösungsorientierte und direkt nutzbare Antworten und kann in den persönlichen Einstellungen von Copilot Chat hinterlegt werden.

#### Die 5 Prompting-Übungen

1. **Iterativer Ansatz** ([Übung](Modul%204%20Copilot%20Prompting/uebung-meeting-zusammenfassen.md))
   Ein Meeting-Transkript wird Schritt für Schritt in ein gutes Meeting-Protokoll überführt.
   Ziel ist zu zeigen, wie man sich interaktiv durch mehrere Prompts an das gewünschte Ergebnis annähert - genau so, wie Menschen typischerweise mit KI arbeiten.

2. **One-Shot-Ansatz** ([Übung](Modul%204%20Copilot%20Prompting/one-shot-prompt-meeting-protokoll.md))
   Ein einzelner, sehr präzise formulierter Prompt erzeugt in einem Durchlauf ein vollständiges, solides und umfassendes Protokoll.
   Solche One-Shot-Prompts stehen für verlässliche und reproduzierbare Ergebnisse.

3. **Few-Shot-Ansatz** ([Übung](Modul%204%20Copilot%20Prompting/uebung-few-shot-prompting.md))
   Mit 2-3 Beispielen im Prompt lernt Copilot Format, Stil und Entscheidungslogik durch Vormachen statt durch lange Regelbeschreibungen. Du vergleichst Zero-Shot und Few-Shot anhand der Klassifikation von Kundennachrichten.

4. **Chain-of-Thought-Prompt:** 
   ***Lehrer-Laempel-Übung*** (möglichst deterministischer Prompt) ([Übung](Modul%204%20Copilot%20Prompting/LehrerLaempelPrompt.md))
   Diese Übung zeigt einen streng regelbasierten **Chain-of-Thought-Prompt**: Vor jeder Antwort durchläuft die KI eine feste Analyse (G-R-O-W) und entscheidet erst dann über Rückfragen oder Ergebnis. Der Prompt hat ein fail-safe Verhalten: Entweder werden fehlende Informationen über Rückfragen geklärt oder mit dem Escape-Word **DIREKT** sofort geliefert. Das Ergebnis ist hochgradig kontrollierbar, reproduzierbar und besonders für professionelle Nutzung geeignet. Gleichzeitig lernst du, wie Governance, Qualitätskontrolle und operative Effizienz in einem einzigen Prompt-Design zusammengeführt werden.

5. **E-Mail-Analyse und Antwortentwurf (Kundenservice)** ([Übung](Modul%204%20Copilot%20Prompting/uebung-email-analyse-antwortentwurf.md))
   Diese Übung trainiert ein 4-Schritte-Modell zur Analyse eingehender E-Mails und zur Erstellung professioneller Antwortentwürfe. Zusätzlich wird das Dokument **Corporate-Wording-Guideline-allgemein.docx** als verbindliche Sprachgrundlage angewendet.

## One-Shot Prompt vs. Skill

Inhaltlich ist ein **Skill** nichts anderes als ein sehr gut aufgesetzter One-Shot Prompt (+ weitere Fähigkeiten, die ein KI-Agent ausführt, z. B. Programmieraufgaben o. ä.).

- Wenn ein **Mensch** einen einzelnen, vollständig formulierten Prompt direkt nutzt, spricht man von einem **One-Shot Prompt**.
- Wenn ein **KI-Agent** denselben Ansatz als wiederverwendbare Anweisung ausführt, spricht man typischerweise von einem **Skill**.

Der Unterschied liegt also primär im **Nutzungskontext** (Mensch vs. Agent), nicht im Grundprinzip des Prompts.

## Direkte Links zu den Übungen und Prompt-Anweisungen

Gehe die Übungen in dieser Reihenfolge durch, um die Unterschiede zwischen iterativem Prompting und One-Shot-Prompting zu erkennen:

   1. **Übung** Iterativ: [uebung-meeting-zusammenfassen.md](Modul%204%20Copilot%20Prompting/uebung-meeting-zusammenfassen.md)
   2. **Übung** One-Shot: [one-shot-prompt-meeting-protokoll.md](Modul%204%20Copilot%20Prompting/one-shot-prompt-meeting-protokoll.md)
   3. **Übung** Few-Shot: [uebung-few-shot-prompting.md](Modul%204%20Copilot%20Prompting/uebung-few-shot-prompting.md)
   4. **Übung** Deterministisch (Chain-of-Thought): [LehrerLaempelPrompt.md](Modul%204%20Copilot%20Prompting/LehrerLaempelPrompt.md)
   5. **Übung** Kundenservice: [uebung-email-analyse-antwortentwurf.md](Modul%204%20Copilot%20Prompting/uebung-email-analyse-antwortentwurf.md)

Zusätzliche besondere Prompts:

   6. Prompt Coach: [prompt-coach.md](Modul%204%20Copilot%20Prompting/prompt-coach.md)
   7. Persönliche Copilot-Chat-Anweisung: [copilot_chat_anweisung.md](Modul%204%20Copilot%20Prompting/copilot_chat_anweisung.md)
   8. Agent E-Mail-Beantworter (mit Skill): [agent-email-beantworter.md](Modul%204%20Copilot%20Prompting/agent-email-beantworter.md)