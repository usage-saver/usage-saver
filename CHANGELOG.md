# Changelog

What changed in each version of Usage Saver, in plain words.

## 0.3.4

- **README:** install steps now use the app's real button names (+ Add → Add from repository → Sync → Add), checked on a phone. It also says plainly that if you already have your own usage-saving skill, you likely don't need this one, since both would load.
- **Tested:** only the README and version numbers changed since 0.3.3 (checked with git diff), so 0.3.3's checks still stand. All 7 version numbers match, the download file matches the repo, and the privacy scan was clean.

## 0.3.3

- **New:** an icon, a gauge with its needle in the green.
- **Tested:** all 7 version numbers match; the download file (now 8 files, with the icon) matches the repo byte for byte; Claude Code's plugin checker passed with the icon found (1 warning left: no author, on purpose); a fresh install worked, still about 110 tokens per session; the icon has no hidden metadata, and white on navy is 11.5:1 contrast; the privacy scan was clean.

## 0.3.2

- **Fixed:** if a chat gets summarized, Usage Saver now loads a skill again, since the summary drops the skill's text.
- **New:** a lighter model or paying with usage credits never skips a check.
- **New tips:** what Team and Enterprise seats get for Fable, the short cache on usage credits in Claude Code, and when to use `/compact` or `/rewind`.
- **README:** exact menu names, an Add marketplace option that keeps it up to date, how to get updates in Claude Code, a warning not to install it twice, and how to pause or remove it.
- **Tested:** every file parses; all 6 version numbers match; the download file matches the repo byte for byte; Claude Code's plugin checker passed (1 warning: no icon yet); a fresh install from the repo worked and adds about 110 tokens per session; the privacy scan was clean on the files, the download and all past commits.

## 0.3.1

- Search modes (quick first, thorough only when needed), what each turned-on skill costs, and more coaching tips.

## 0.3.0

- Tips for reused text, Projects and batching edits and work.

## 0.2.1

- First public version: the save-usage skill with its coding playbook, plus `/handoff` and `/lean`.
- Claude Code install through the marketplace file, a downloadable plugin file, the CC0 license, and automatic version tags.
