# Usage Saver

A free Claude plugin that makes your usage last longer. It teaches Claude to skip wasted work (rereading huge files, rewriting whole documents, long rambling replies, needless searches) while keeping every check and every bit of quality.

It's only instructions: no code, nothing runs on your computer, and nothing is collected or sent anywhere. Free, with no accounts and no tracking. It's built to be light itself, so it doesn't eat the usage it's saving. It works on any paid plan, from Pro to Ultra, and with any model, including the top ones.

Version 0.3.1

## What's inside

| Skill | What it does |
|---|---|
| **save-usage** | Turns on by itself for bigger tasks. Cuts waste in reading, writing, research and replies. After your first message, it tells you if a lighter or heavier model fits better, and respects your choice if you prefer the top models. For coding tasks, it also follows a built-in coding playbook (understand first, small changes, real tests, clean finish) that only loads when there's code involved. |
| **/handoff** | Writes a short note to paste into a fresh chat, plus which model to open it on. |
| **/lean** | Makes the rest of a chat extra-lean: shortest answers, no extras. Say "lean off" to go back. |

## Install

### In the Claude app

1. Download [usage-saver.plugin](https://github.com/usage-saver/usage-saver/raw/main/usage-saver.plugin).
2. In Claude, open **Customize**, then **Plugins**, choose the upload option, and pick the file.
3. Done. It's saved to your account, so it also works in chat and in Claude Code.

If the upload won't take a `.plugin` file, rename it to `usage-saver.zip` and try again. It's the same file.

### In Claude Code

```
/plugin install usage-saver --marketplace usage-saver/usage-saver
```

On older versions of Claude Code, run `/plugin marketplace add usage-saver/usage-saver`, then `/plugin install usage-saver@usage-saver`.

## Free cheat sheet

Reading this costs no usage at all.

### Pick a model before you start

| Tier | Today's example | Fits |
|---|---|---|
| Heavy | Opus 5.5, high or extra-high effort | Planning a build, new features, tricky bugs, careful reviews, hard writing or analysis |
| Middle | Sonnet 5.5, default effort | Everyday chats, small fixes and chores, drafts, quick research. The best default. |
| Light | Haiku 5.5 | Tiny one-off questions with no code, files or research: a fact, a conversion, a quick rewrite |
| Top | Fable 5.2, or any model at max effort | The hardest problems: big architecture, deep debugging, long complex analysis, or when the heavy tier fell short |

Pick at the start. Switching models mid-chat makes Claude read the whole chat again at full cost. Model names change over time, so match newer ones to the same tiers.

Love the top models? Just tell Claude. It won't nudge you down, except once for a clearly tiny task or when you're near a limit.

### Your plan

- **Pro:** Fable runs on usage credits from your first message. Set a monthly spend limit before you try it.
- **Max and Ultra:** Fable is included for up to half your weekly limits, and it uses them faster than other models. Save it for your hardest work, and use Opus or Sonnet for everyday stuff to keep more of your week free.
- **Every plan:** cutting waste matters just as much on big plans. It's what lets your favorite model go further.
- Plans and limits change. Settings → Usage always shows where you stand.

### Biggest savers

- Start a fresh chat for each new job. Long chats get re-read with every message. `/handoff` makes it easy.
- Coming back to a long chat after hours away? Start fresh with `/handoff` instead.
- Put related questions in one message.
- Keep one fixed opening message for each kind of work (the task goes at the end), so every chat starts the same way, on the right model.
- Group edits to your instructions or skills into one sitting. Each change resets the cache once.
- To fix a request, edit your last message instead of sending a correction.
- Paste text instead of screenshots when only the words matter, and share only the PDF pages you need.
- Research mode and web searches use a lot. Skip them when you don't need them.
- Close to your limit? Type `/lean` to make the rest of the chat extra-lean.

### Settings worth a look

- Turn off web search, connected apps and skills a chat doesn't need.
- Settings → Usage shows where your limits stand. If your plan has a 5-hour window, start big jobs early in a fresh one.
- On usage credits, set a monthly spend limit and keep auto-reload off (Settings → Usage → Usage credits).
- Set a weekly reminder to glance at Settings → Usage, so your limit never surprises you.

### If you use Projects

- Keep Project instructions short. Files you use again and again belong in the Project, where they're cached.
- Files that change often are better left where they live, with a short pointer in the instructions. A stale copy costs usage and can mislead.
- Put what rarely changes at the top of instructions and opening messages, and what changes at the bottom, since caching matches from the top.
- If your Claude has it, ask "explain my usage" after a session to see where it went.

## Good to know

- Claude can't switch models for you. When it suggests one, tap the model picker.
- It never skips a check or test to save usage. If a saving would weaken quality, it doesn't take it.
- Already have your own usage-saving skill or rules? Yours win. Usage Saver steps back from anything yours covers, so nothing gets done twice, and only fills gaps yours leaves. You can still turn it off if you'd rather not have it at all, since every turned-on skill adds a little to every message.

## Remove it

Open **Customize**, then **Plugins**, then **Usage Saver**, and choose **Remove**.

## License

Public domain under [CC0 1.0](LICENSE). Use it, change it and share it however you like. No credit needed.
