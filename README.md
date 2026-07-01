# LMS Copilot Basics - Öffentliche Ausschnitte

Dieses Repository zeigt öffentlich verfügbare Auszüge aus dem Learning Management System **Copilot Basics**.

Das komplette LMS **Copilot Basics** ist eine umfassende Schulung mit **14 Modulen** und **88 Lernsessions**. In diesem Repository werden bewusst nur einzelne Ausschnitte bereitgestellt, um Einblicke in Aufbau, Methodik und Prompting-Praxis zu geben.

## Modul 4: Copilot Prompting

In [Modul 4 Copilot Prompting](Modul%204%20Copilot%20Prompting/) findest du eine Prompting-Übung mit drei Ansätzen:

1. **Iterativer Ansatz**
   Ein Meeting-Transkript wird Schritt für Schritt in ein gutes Meeting-Protokoll überführt.
   Ziel ist zu zeigen, wie man sich interaktiv durch mehrere Prompts an das gewünschte Ergebnis annähert - genau so, wie Menschen typischerweise mit KI arbeiten.

2. **One-Shot-Ansatz**
   Ein einzelner, sehr präzise formulierter Prompt erzeugt in einem Durchlauf ein vollständiges, solides und umfassendes Protokoll.
   Solche One-Shot-Prompts stehen für verlässliche und reproduzierbare Ergebnisse.

3. **Lehrer-Laempel-Übung (Deterministischer Kontroll-Prompt)**
   Diese Übung zeigt einen streng regelbasierten Prompt mit fail-safe Verhalten: Entweder werden fehlende Informationen über Rückfragen geklärt oder mit dem Escape-Word **DIREKT** sofort geliefert. Das Ergebnis ist hochgradig kontrollierbar, reproduzierbar und besonders für professionelle Nutzung geeignet. Gleichzeitig lernst du, wie Governance, Qualitätskontrolle und operative Effizienz in einem einzigen Prompt-Design zusammengeführt werden.

## One-Shot Prompt vs. Skill

Inhaltlich ist ein **Skill** nichts anderes als ein sehr gut aufgesetzter One-Shot Prompt (+ weitere Fähigkeiten, die ein KI-Agent ausführt, z. B. Programmieraufgaben o. ä.).

- Wenn ein **Mensch** einen einzelnen, vollständig formulierten Prompt direkt nutzt, spricht man von einem **One-Shot Prompt**.
- Wenn ein **KI-Agent** denselben Ansatz als wiederverwendbare Anweisung ausführt, spricht man typischerweise von einem **Skill**.

Der Unterschied liegt also primär im **Nutzungskontext** (Mensch vs. Agent), nicht im Grundprinzip des Prompts.

## Direkte Links zu den Übungen

Gehe die Übungen in dieser Reihenfolge durch, um die Unterschiede zwischen iterativem Prompting und One-Shot-Prompting zu erkennen:
  1. Iterativ: [uebung-meeting-zusammenfassen.md](Modul%204%20Copilot%20Prompting/uebung-meeting-zusammenfassen.md)
  2. One-Shot: [one-shot-prompt-meeting-protokoll.md](Modul%204%20Copilot%20Prompting/one-shot-prompt-meeting-protokoll.md)
   3. Deterministisch: [LehrerLaempelPrompt.md](Modul%204%20Copilot%20Prompting/LehrerLaempelPrompt.md)
