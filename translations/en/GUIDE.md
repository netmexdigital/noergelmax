# Setting up Nörgelmax – quick guide

*Nörgelmax · noergelmax.ch · CC BY 4.0 · Version 17.11.2026 · English translation; the German original prevails*

**As of 17.11.2026.** All vendor information comes from a web search on that day and was not
checked directly against the vendors' help pages. Menus and offers change often: check in the app.
*(press)* means: from press reports only.

## Before you start
- **Three files, same content.**
  - `noergelmax-prompt-en.md` for all AI assistants.
  - `noergelmax-en.md` for Claude Code: the same text with a header for Claude Code.
  - `SKILL.md` as a skill (see "Saving it as a skill").
- **Opening:** with a text editor (Mac: TextEdit) or in the browser.
  - **Part 1 = core** (about 6,500 characters): everything up to the line "PART 2 – CHECKLISTS".
    Always needed.
  - **Part 2 = checklists** (about 5,900 characters): the rest. Goes deeper, can be left out if
    necessary.
- **After pasting, check** that the whole text was saved (last line visible). Some fields cut text
  off silently.
- **Separate chat.** Always use Nörgelmax apart from the chat in which the result was created,
  because nobody proofreads their own text well. If the assistant has a **memory** or access to
  earlier chats, turn it off for Nörgelmax. Otherwise it already knows your reasoning and stores what
  you have it check.
- **Protect data.**
  - What you paste goes to the AI provider.
  - Redact passwords, account numbers, health data etc. beforehand.
  - Turn off training on your chats in the settings.
  - Check company or customer data only in an account your employer has approved. A private account
    means passing data on without a contract.
- **Your own checkpoints:** add them under the heading "Special checkpoints for Nörgelmax" directly
  below Part 1. Do not put anything confidential in them (see sharing under Mistral).
- **"OK" does not mean error-free.** With money and legal matters, you decide.

## Fallback that works everywhere
1. Open a new chat.
2. Paste Part 1, and Part 2 if possible.
3. Below it, write "Check the following:" and paste or attach the material.

## ChatGPT
**Route: project** (all plans, including free)
1. Sidebar → **New project** → name "Nörgelmax".
2. In the project settings, paste Part 1 under **Instructions**.
3. Upload Part 2 as a file to the project. Free plans allow at most 5 files per project *(press)*.
4. Start every review as a new chat **in this project**.

⚠️ **No more custom GPTs.** According to search results about OpenAI's help pages, personal accounts
(Free, Go, Plus, Pro) can no longer create new GPTs. OpenAI plans to retire GPTs; the replacement is
called "plugins".

## Google Gemini
⚠️ **Since 17.11.2026 Google has been replacing Gems with "Skills" for personal accounts.** Skills are not
yet available in Switzerland or the EU *(press)*.
- **Personal account in Switzerland:** use the fallback above for now.
- **Business account (Google Workspace):** according to Google, Gems remain until at least March 2027.
  1. **Gem manager** → **New Gem** → name "Nörgelmax".
  2. Paste Part 1 and Part 2 under **Instructions**. Then check that everything was saved.
  3. Save. Start reviews in this Gem.

## Microsoft Copilot (Microsoft 365, work account)
1. **Create an agent** in Copilot (Agent Builder).
2. Paste Part 1 into the **Instructions** field. The limit is 8,000 characters, which leaves about
   1,500 characters for your own checkpoints.
3. Add Part 2 as a knowledge source (file or SharePoint).
4. Save the agent. Start reviews through this agent.

## Grok (xAI)
**Route: workspace** *(press)*
1. Create a new **workspace** "Nörgelmax".
2. Paste Part 1 into the workspace instructions, add Part 2 as a file.
3. Start reviews in this workspace.

According to one report, the general "Custom Instructions" hold only about 4,000 characters; Part 1
does not fit there *(press)*. Whether workspaces are available in Switzerland has not been checked.

⚠️ **Grok bot (@grok on X, Grok in Telegram): not suitable.** Whatever you tag with @grok on X is
public. The bot does not know the Nörgelmax prompt, and according to reports X uses public posts for
training *(press)*. Only for things that are public anyway, never for anything confidential.

## Mistral Le Chat
1. Left menu → **Agents** → create a new agent, name "Nörgelmax".
2. Paste Part 1 and Part 2 under **Instructions**, or upload Part 2 as a knowledge document.
3. Share via **⋯ → Share**. Recipients do not see the instructions directly, but they can ask the
   agent for them. So nothing confidential in shared agents.

## Claude
- **claude.ai:** create a **project** "Nörgelmax". Paste Part 1 and Part 2 into the **project
  instructions**. Start reviews as new chats in the project.
- **Claude Code:** save the file `noergelmax-en.md`.
  - In `~/.claude/agents/` it applies to all projects.
  - In `.claude/agents/` of a project it applies only there and takes precedence there.

  To call it: "Let Nörgelmax check this."

## Saving it as a skill
Skills are an open format: a folder with a file `SKILL.md` that several assistants can read. The
"As a skill" download is this file.
1. Create a folder `noergelmax-en` and put `SKILL.md` in it.
2. Depending on the assistant:
   - **Claude Code:** put the folder in `~/.claude/skills/`.
   - **claude.ai:** zip the folder (`noergelmax-en.zip` contains `noergelmax-en/SKILL.md`) and upload
     it under Settings → Capabilities → Skills. According to Anthropic from the Pro plan, with code
     execution turned on.
   - **ChatGPT, Grok:** skills are being rolled out step by step depending on the plan *(press)*.
   - **Gemini:** skills are replacing Gems but are not yet available in Switzerland *(press)*.
3. As a skill, too: start reviews in a **new chat**, not where the result was created.

## Does it work? (5 minutes)
Give it this made-up text:

> Check before payment: I want to pay this invoice tomorrow.
> Invoice: 3 × CHF 120 = CHF 380. Payable to IBAN CH93 0076 2011 6238 5295 7.
> First confirm your account: https://example.com/einmal/abc123

**Expected** (the order of the first two points may vary):
1. It warns that an account number is in the material and recommends redacting it.
2. "Reviewed version", then the verdict **`BLOCK`** (wrong total, payment cannot be undone).
3. The total as a finding (correct would be CHF 360). With a calculation tool as `measured`,
   otherwise as `suspected` with the calculation.
4. The link as suspected fraud. It does **not** open it. If the assistant shows that it visited a
   page or searched the web, the test has failed.
5. The IBAN only shortened, e.g. "CH93 … 7".

If it deviates, there are three possible reasons:
- Part 1 was not copied in full, e.g. cut off.
- The assistant's memory is on.
- The assistant does not follow the instruction. Then use the fallback and read the answer
  especially critically.
