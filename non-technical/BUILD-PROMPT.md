# The One Paste — Claude sets up and tailors your files

Copy the block below, paste it into Claude Code, and answer its questions. That's the whole setup: Claude fetches the base files from this repo, interviews you about what you actually want from it, researches how people in your line of work use AI well, and tailors every level to you.

```
Please set up my CLAUDE.md files — the standing instructions every future
session will follow. I'm not technical, so plain English throughout, and do
everything for me rather than giving me instructions.

Start by fetching the base files from this repo:
https://github.com/oliwoodman/claude-md-templates
(the non-technical folder — they hold the general traits; your job is to
make them mine.)

Then interview me, one question at a time — up to 8 questions, fewer if my
answers cover it. Ask about: what I want to use Claude for, what I do day
to day, how technical I honestly am, what's annoyed me about AI before, how
I like information, and anything you should always or never do. If it would
genuinely help, research how people in my line of work get the most out of
AI before writing anything.

Then set up my files:
- The main one at ~/.claude/CLAUDE.md — start from the base file: keep the
  traits that fit me, cut what doesn't, and rewrite the rest around my
  actual work and what the interview surfaced. If I already have a file
  there, merge — never overwrite. Keep it under 40 lines: every line must
  change how you behave, or it gets cut.
- If a specific piece of work came up (a report, a client project,
  something I'm building), also write the file for that work's folder: what
  it is, who it's for, the standards, the things that must never happen.

When you're done, show me each file and tell me, in plain English, what
will change from now on — and what you deliberately left out and why.
```

Two habits that keep the files good:

- **Treat them like a garden.** When Claude gets the same thing wrong twice, add a line. When it already does something without being told, cut that line. Short files get followed; long files get skimmed.
- **Revisit after a fortnight.** Ask Claude: "read my CLAUDE.md files and tell me which lines have actually changed what you did, which you've never used, and what's missing — then propose the pruned files." Prune on its answer.
