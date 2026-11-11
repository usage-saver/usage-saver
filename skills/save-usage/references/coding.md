# Coding playbook

Excellent code is the biggest usage saver: work done right the first time never has to be redone. The user's own instructions and the project's rules win any conflict with this playbook.

## Before changing anything

- **Learn the project's rules first:** README, CONTRIBUTING, CLAUDE.md or AGENTS.md, any notes file, and the project's own test, lint and build commands (package.json scripts, Makefile, pyproject and the like). Use those rather than inventing new ones.
- **Read just enough:** search for the code involved, then read it plus its callers, its tests and similar code nearby. Match the existing style, naming and patterns.
- **Bugs:** reproduce first, with a failing test or the smallest repro. Fix the cause, not the symptom.
- **Don't guess:** if unsure how a library, API or platform feature behaves, check the docs for the version actually installed, or try it in a tiny script.
- **Plan:** anything beyond a small fix gets a short plan first: the files to touch, the approach, and how it will be checked.

## While changing

- **Smallest change that does the job.** No drive-by refactors, renames or reformatting; suggest them instead.
- **Clear structure:** logic separate from screens and I/O so it can be tested on its own, small functions with one job each, clear names, and comments that explain *why* only where it isn't obvious.
- **One source of truth** for every value and setting.
- **Fail on purpose:** clear error messages and a way forward. No silent catches, no blank screens.
- **Safe by default:** no secrets in code, input checked at the edges, dependency versions pinned, and a new dependency only when it clearly earns its place.
- **Efficient edits:** batch related edits to a file in one pass, and run independent reads and searches in parallel.

## Checking (never skipped)

- **Run it.** Never call code tested unless it actually ran.
- **Narrow, then wide:** run the most relevant tests first, then the full suite plus the linters and type checks the project uses. Read a failure carefully once and fix its cause.
- **Awkward cases:** empty input, errors, large input, old saved data, and for screens a small phone size and dark mode if supported. Look at screenshots of visual changes.
- **Trace the change:** find everything that depends on what changed (callers, tests, docs, config, saved data) and make sure it all still agrees.
- **Review your own diff** before finishing: leftover debug lines, dead code, inconsistent names, unrelated changes.

## Debugging

- Read the whole error and stack trace once, and find the first line in the project's own code.
- Narrow it down instead of guessing: a smaller input, `git bisect`, or switching parts off one at a time.
- Add targeted logging, then remove it when done.

## Saving work

- Commit in small working steps with clear messages, when the user wants commits. Ask before pushing, force-pushing, deleting, or anything hard to undo.
- Before a big or risky change, make sure the last working version is saved.
- For work spanning chats, keep a short notes file (where things stand, decisions and why, what's next), so `/handoff` stays tiny.

## Usage-smart habits

- Shallow clones (`git clone --depth 1`) unless history is needed.
- Quiet output: `-q`, `--silent`, `| tail -20`, failures only, and `git log --oneline -5` instead of full logs.
- Use a task list for multi-step work, so progress survives without re-reading the chat.
- In Claude Code, run `/compact` at a natural break between tasks, not mid-task. To drop a wrong path, `/rewind` to before it instead of correcting it: rewinding reuses the cache, compacting rebuilds it.

## Finishing

Say what changed, what was checked and how, and what couldn't be checked. Be plain about anything uncertain.
