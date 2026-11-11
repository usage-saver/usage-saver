---
name: handoff
description: For /handoff or "continue in a new chat". Writes a short note to paste into a fresh chat, plus which model to open it on.
metadata:
  version: "0.3.6"
---

# Handoff

Get the work ready to continue in a fresh chat. Every message re-sends the whole chat, so a fresh chat costs far less per message than a long one.

1. **Save what matters first.** If the project keeps a notes file (like `PROGRESS.md`), update it: where things stand, what was decided and why, and what's next. Ask before committing or pushing it anywhere.
2. **Write the note** in one code block so it's easy to copy, under 150 words:
   ```
   Continue <project or task>.
   Where things stand: <one or two lines>.
   Decided: <key decisions, each with a short why>.
   Where it lives: <files, folders, repos or links>.
   Today: <the one next task>.
   ```
   If a notes file exists, point to it instead of repeating it: `Read <notes file> in <place> first.`
3. **Name the model** in one line: top (Fable today, or max effort) for the hardest problems; heavy (Opus today) for planning, real builds and hard problems; middle (Sonnet today) for everything else; light (Haiku today) for tiny questions. If the user prefers a heavier model, go with that.
4. **Say how:** copy the note, start a new chat, pick that model, paste it in.

Leave out anything the fresh chat can find in the files. Never put passwords, keys or tokens in the note or the notes file.
