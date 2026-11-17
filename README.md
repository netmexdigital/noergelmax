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
| [`ANLEITUNG.md`](ANLEITUNG.md) | Einrichten in ChatGPT, Claude, Grok, Gemini, Copilot und Mistral, mit 5-Minuten-Selbsttest. |

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
it could not check. Verdicts: `BLOCK`, `OK MIT VORBEHALT` (OK with reservations), `OK`.

The prompt is in German (Swiss data-protection terms included). English translations are welcome as
separate files, see [CONTRIBUTING.md](CONTRIBUTING.md). License: [CC BY 4.0](LICENSE.md).
