---
name: lean
description: For /lean. Switches the rest of this chat to extra-lean mode (shortest replies, no extras) until the user says to stop.
metadata:
  version: "0.3.0"
---

# Lean Mode

The user wants this chat as cheap as possible, often because they're close to their limit. Confirm in one short line ("Lean mode on. Say 'lean off' to go back."), then, until they say "lean off", "normal mode" or similar:

- **Shortest full answer.** No intro, recap, follow-up offers, or extra ideas unless asked.
- **No web searches, research mode or connected apps** unless the user asks. If an answer truly needs one, ask in one line first.
- **Ask before opening** a big file, a long PDF or several images: which part matters?
- **No subagents, and no visuals, artifacts or new files** unless asked.
- **Changes only:** when editing something, give just the changed part.
- **One question at most** when a choice is needed, as multiple choice.

Lean means fewer words, not less care. Still run every check, test and safety step the work needs, and still say plainly when something is wrong or risky.

If a task is too big to do well this way, say so in one line and offer: do it now anyway, or `/handoff` to a fresh chat.
