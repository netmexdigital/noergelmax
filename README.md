# Nörgelmax – der unbequeme Gegenprüfer

![Nörgelmax, ein grimmiger Gartenzwerg mit verschränkten Armen](assets/noergelmax.jpg)

**Nörgelmax** ist ein Prompt für KI-Assistenten. Er heisst ein Ergebnis nicht gut, er versucht es zu
**widerlegen**: Programmcode, Texte, Mails, Pläne, Entscheide, Tabellen und Abrechnungen, dazu
Sicherheit, Datenschutz und der Schutz von Personen. Zu jedem Mangel liefert er einen Lösungsweg und
sagt offen, was er nicht prüfen konnte.

Website: [noergelmax.ch](https://noergelmax.ch)

## Dateien

| Datei | Wofür |
| --- | --- |
| [`noergelmax-prompt.md`](noergelmax-prompt.md) | Der Prompt für alle KI-Assistenten. Teil 1 = Kern (immer), Teil 2 = Prüflisten (wenn Platz ist). |
| [`claude-code/noergelmax.md`](claude-code/noergelmax.md) | Derselbe Text als Agent für Claude Code (`~/.claude/agents/`). |
| [`skill/noergelmax/SKILL.md`](skill/noergelmax/SKILL.md) | Derselbe Text als Skill (offenes Format `SKILL.md`). |
| [`skill/noergelmax-skill.zip`](skill/noergelmax-skill.zip) | Der Skill als fertiges ZIP zum Hochladen in claude.ai. |
| [`ANLEITUNG.md`](ANLEITUNG.md) | Einrichten in ChatGPT, Claude, Grok, Gemini, Copilot und Mistral, mit 5-Minuten-Selbsttest. |
| [`translations/en/`](translations/en/) | Englische Fassung: Prompt, Claude-Code-Agent, Skill (`noergelmax-en`) und Kurzanleitung (`GUIDE.md`). |

## In drei Schritten

1. `noergelmax-prompt.md` öffnen.
2. Teil 1 als Anweisung in einem eigenen Projekt, Workspace oder Agenten deiner KI einfügen, als
   Skill speichern, oder am Anfang eines neuen Chats einfügen.
3. Darunter schreiben: «Prüfe Folgendes:» und das Material einfügen.

Nutze Nörgelmax in einem eigenen Chat, nicht dort, wo das Ergebnis entstanden ist. Was du einfügst,
geht an den KI-Anbieter: Passwörter, Kontonummern und Gesundheitsdaten vorher schwärzen. Die Regeln
im Prompt sind Anweisungen an die KI, keine technischen Sperren.

## Mitmachen

Verbesserungen sind willkommen, als Issue oder Pull Request. Siehe [CONTRIBUTING.md](CONTRIBUTING.md).

## Lizenz

[CC BY 4.0](LICENSE.md). Frei verwendbar und anpassbar, mit Nennung «Nörgelmax, noergelmax.ch».
Ohne Gewähr: Nörgelmax ersetzt weder deine eigene Prüfung noch eine Rechts- oder Sicherheitsberatung.
«OK» heisst nicht fehlerfrei.

Ein Projekt der netmex digital gmbh, Aarau (Schweiz).

---

## English summary

**Nörgelmax** (German for roughly "Max the Grumbler") is a reviewer prompt for AI assistants. Instead of
approving a result, it tries to **refute** it: code, texts, emails, plans, decisions, spreadsheets and
accounting, plus security, data protection and personal safety. Every finding comes with a concrete
failure scenario, an evidence level (measured, read, or suspected) and a fix, and the prompt lists what
it could not check. Verdicts: `BLOCK`, `OK WITH RESERVATIONS` (German original: `OK MIT VORBEHALT`), `OK`.

**English version:** [`translations/en/noergelmax-prompt.md`](translations/en/noergelmax-prompt.md), plus a
Claude Code agent ([`translations/en/claude-code/noergelmax-en.md`](translations/en/claude-code/noergelmax-en.md))
and a skill ([`translations/en/skill/noergelmax-en/SKILL.md`](translations/en/skill/noergelmax-en/SKILL.md),
ready-made ZIP for claude.ai: [`translations/en/skill/noergelmax-en-skill.zip`](translations/en/skill/noergelmax-en-skill.zip)),
plus a quick guide for ChatGPT, Claude, Grok, Gemini, Copilot and Mistral with a 5-minute self-test:
[`translations/en/GUIDE.md`](translations/en/GUIDE.md). Website in English: [noergelmax.ch/en](https://noergelmax.ch/en/).
The German original prevails; the translation follows it.

Part 1 (core, about 6,500 characters) goes into your assistant's instructions, Part 2 (checklists) is
appended or uploaded as a file. Use it in a separate chat, not the one where the result was created.
What you paste goes to the AI provider: redact passwords, account numbers and health data first, and
turn off the assistant's memory for it. The rules in the prompt are instructions to the AI, not
technical locks.

No warranty: Nörgelmax does not replace your own review or legal or security advice. "OK" does not
mean error-free.

Improvements are welcome, see [CONTRIBUTING.md](CONTRIBUTING.md). License: [CC BY 4.0](LICENSE.md).
