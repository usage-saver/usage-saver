---
name: save-usage
description: Load at the start of any task beyond a quick question (code, files, documents, research). Saves usage by cutting waste, never quality.
metadata:
  version: "0.3.6"
---

# Save Usage

Cut wasted work so the user's usage lasts longer. Never cut quality.

## The one rule

Skip *wasted* work, never real work. The user's own instructions and their other skills win every conflict: every test, review and check still happens in full. If a saving would weaken one, don't take it. Work done right the first time is the cheapest.

## Their own rules win

If the user already has their own usage-saving skill, plugin or rules (in their instructions, preferences or another skill), theirs win. Follow theirs and don't repeat or restate what they cover, so nothing is done twice. Use this skill only for ground theirs is silent on, and drop any advice here that clashes with theirs. If it's unclear whether something overlaps, leave it out. The `/handoff` and `/lean` commands still work when the user types them.

## Where usage goes

- Every message re-sends the whole chat. Caching makes the unchanged part cheap, but only while it's warm. After a long break, the whole chat is read again at full cost.
- Switching models mid-chat restarts the cache. Loading a skill doesn't, since it's added at the end.
- The big costs: long chats, big files and images, long tool output, writing long text or code, web searches, subagents, and redoing work.

## Model and effort

| Tier | Today's example | Fits |
|---|---|---|
| Heavy | Opus 5.5, high or extra-high effort | Planning a build, new features, tricky bugs, careful reviews, hard writing or analysis |
| Middle | Sonnet 5.5, default effort | Everyday chats, small fixes and chores, drafts, quick research. The best default. |
| Light | Haiku 5.5 | Tiny one-off questions with no code, files or research: a fact, a conversion, a quick rewrite |
| Top | Fable 5.2, or any model at max effort | The hardest problems: big architecture, deep debugging, long complex analysis, or when the heavy tier fell short |

Model names change; map newer models to the same tiers.

- **After the user's first message:** if the model or effort doesn't fit the task, say so in one line and name the one that fits. The user switches it; Claude can't. If it fits, say nothing. If the effort setting isn't visible, name the right one without guessing theirs.
- **Respect their choice.** If the user prefers a heavier model or max effort, don't nudge them down. Mention a lighter one only when the task is clearly tiny or they're near a limit, and only once.
- If a chore chat turns into a real build (or the other way around), suggest switching once, or `/handoff` to a fresh chat on the right model.
- A lighter model or paying with credits never drops a check: every test and review still runs in full.

## Plans

Fit the advice to the user's plan when it's known. Plans and limits change, so when unsure, point to Settings → Usage rather than guessing.
- **Pro:** Fable runs on usage credits from the first message. Before suggesting it, say it costs credits.
- **Max and Ultra:** Fable is included for up to half the weekly limits, and it uses them faster than other models. Use it for the hardest work; for everyday tasks, a lighter model keeps more of the week free.
- **Team and Enterprise:** standard seats work like Pro for Fable, and premium seats like Max.
- **Paying with usage credits:** use the middle tier for anything that isn't a real build. Before anything big, say in one line how heavy it is and ask: do it now on credits, or wait for the reset. In Claude Code the cache lasts only about five minutes on credits (about an hour within plan limits), so keep credit-paid work in one sitting.
- **Every plan:** cutting waste matters just as much on big plans. It's what lets heavy and top-tier models go further.

## Files, images and documents

- **Search, then read.** Find the part that matters and read only that. Read big files and long PDFs in sections, never whole.
- Screenshots and PDF pages cost far more than the same words as text. If the user is about to share many of them and only part matters, suggest the text or just the pages needed, once.
- Don't re-read a file you just wrote. Re-read only if it may have changed.
- **Change, don't rewrite.** Edit only what changes; never regenerate a whole file, document or artifact for a small fix. Send long content as a file instead of pasting it into the chat.
- **Memory:** if Claude keeps memory files, read only the ones that bear on the task, several in one call.
- **Code tasks:** read `references/coding.md` in this skill's folder once at the start, and follow it.

## Working

- **Plan before building** anything beyond a small fix. Rework is the biggest waste.
- **Ask once, up front:** gather real choices into one set of multiple-choice questions (up to 4), not one per message.
- **Research:** one search per fact, more only when needed. Prefer official docs, fetch a page only when the snippet isn't enough, and never repeat a search. If search has a quick and a thorough mode, use the quick one first, and the thorough one only when quick comes back thin or the fact is very new or niche.
- Load every skill and tool the task needs in one parallel step. Skip the ones it doesn't need, and don't reload a skill already in the chat, unless the chat was summarized since (its text is gone then).
- **Checks run in full, but quietly:** one combined command that prints pass/fail and the failures, not full logs.
- If the same fix fails twice, stop and rethink, or ask.
- No subagents unless the user asks. If one would truly help, ask first and say it costs more.

## Replies

- Lead with the answer and keep it short. Don't restate the request, recap steps, narrate between them, or repeat what a card or file already shows.
- End with what changed, what was checked, and one next step if there is one.
- After a big session, add one line on what used the most and how to cut it next time.

## Chat size

- **One chat, one job.** When a job is done and the next is unrelated, or the chat is long, offer `/handoff`. Offer it too when the user comes back to a long chat after hours away.
- Before anything big, say so in one line. If it's huge, ask: do it all now, split it across chats, or start with a lighter version. No option drops a check.

## Reused text and Projects

Caching matches from the top, so wherever text gets reused (custom instructions, Project instructions, opening messages, status notes), steady parts go first and changing parts last.
- **Projects** hold steady files the user reuses, where they're cached and count less each time. Files that change often stay where they live (a repo, a drive), and the Project's instructions just point there. A stale copy costs usage and can mislead.
- **Status notes and handoffs:** a short steady brief on top, the current status below, and history in a changelog rather than piling up in the notes.
- **Batch edits:** each change to custom instructions or skill descriptions resets the cache, so suggest grouping them into one sitting.
- **Batch work:** suggest doing related tasks back to back while the cache is warm.

## Tips

At most one per chat, and only when it fits what just happened:
- Put related questions in one message. To fix a request, edit your last message instead of sending a correction.
- Keep one fixed opening message for each kind of work, with the task at the end, and open it on the model that fits.
- Turn off web search, connected apps and skills a chat doesn't need. Every turned-on skill adds its description to every message, so turn off any that go unused for a couple of months.
- Research mode and web searches use a lot. Skip them when a chat doesn't need them.
- Paste text instead of screenshots when only the words matter, and share only the PDF pages you need.
- Settings → Usage shows where the limits stand. If the plan has a 5-hour window, start big jobs early in a fresh one.
- On usage credits, set a monthly spend limit and keep auto-reload off (Settings → Usage → Usage credits).
- Close to your limit? Type `/lean` to make the rest of the chat extra-lean.
- If this Claude has it, ask "explain my usage" after a session to see where it went.

The plugin's README has a free cheat sheet (model picker and tips) that costs nothing to read.
