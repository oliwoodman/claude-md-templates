# The Build Prompt — have Claude write your files with you

Paste this into Claude Code (or a Claude chat with your folder connected). Claude interviews you about what you actually want from it, researches how people in your line of work use AI well, and writes your files — starting from the base files in this repo, not from a blank page.

```
I want you to build my CLAUDE.md files — the standing instructions every
future session will follow. I'm not technical, so plain English throughout.

Start by fetching the base files from this repo:
https://github.com/oliwoodman/claude-md-templates
(the non-technical folder — they hold the general traits; your job is to
make them mine.)

Then interview me, one question at a time, up to 8 questions. Cover:
- what I want to use Claude for (my work, a side project, life admin,
  building something)
- what I do day to day, so everything gets pitched at my world
- how technical I honestly am
- what has annoyed me or gone wrong with AI before
- how I like information: short and direct, or talked through
- anything Claude should always do, or never do

Where it would genuinely help, research how people in my line of work get
the most out of AI before you write anything.

Then write my files:
- ~/.claude/CLAUDE.md — start from the base file: keep the traits that fit
  me, cut the ones that don't, rewrite the rest in terms of my actual work,
  and add what the interview surfaced. Keep it under 40 lines. Every line
  must change how you behave — if a line wouldn't, cut it.
- If a specific piece of work came up in the interview (a report, a client
  project, something I'm building), also write a CLAUDE.md for that work's
  folder: what it is, who it's for, the standards, the things that must
  never happen.

Show me each file before saving it, explain in plain English what each
section will change about how you work with me, and tell me what you
deliberately left out and why.
```

Two habits that keep the files good:

- **Treat them like a garden.** When Claude gets the same thing wrong twice, add a line. When it already does something without being told, cut that line. Short files get followed; long files get skimmed.
- **Revisit after a fortnight.** You'll know by then which rules are earning their keep. Ask Claude: "read my CLAUDE.md and tell me which lines you've actually used this session" — then prune.
