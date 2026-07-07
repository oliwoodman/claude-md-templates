# The Three-Tier CLAUDE.md Templates

Claude reads your CLAUDE.md files before every single prompt — they're its standing orders. Most people know about one, in the project root. There are actually three tiers, and the difference is reach:

| Tier | Lives at | Applies to |
|---|---|---|
| **Computer** | `~/.claude/CLAUDE.md` | Every project you ever open |
| **Project** | `your-project/CLAUDE.md` | This project, every session, shared with your team via git |
| **Folder** | `any-folder/CLAUDE.md` | Just that corner — only loaded when Claude works in there |

The test for where a rule goes: true for everything you build? Computer. True for this project? Project. True for one corner of it? Folder. A rule lives at exactly one tier — the highest one where it's still true — because the files add together, they don't override each other.

This repo holds a starter template for each tier, plus the prompt that gets Claude to write yours properly.

## For non-technical professionals

The most asked question after these templates went out: "does any of this work if I'm not technical?" Yes — because the file was never about code. It's standing orders, and yours are ways of thinking: plain English, one question at a time, push back when I'm wrong.

The [non-technical folder](non-technical/) holds a full set written by Fable before it left: the main file of general traits, plus project and folder versions for when a specific piece of work needs its own rules. There are no steps to follow — one paste does everything. Claude fetches the files, interviews you (one question at a time) about what you actually want from it, researches your line of work where it helps, and tailors every level to you:

```
Please set up my CLAUDE.md files — the standing instructions every future
session will follow. I'm not technical, so plain English throughout, and do
everything for me rather than giving me instructions.

Start by fetching the base files — the raw versions live here:
https://raw.githubusercontent.com/oliwoodman/claude-md-templates/main/non-technical/CLAUDE.md
https://raw.githubusercontent.com/oliwoodman/claude-md-templates/main/non-technical/project/CLAUDE.md
https://raw.githubusercontent.com/oliwoodman/claude-md-templates/main/non-technical/folder/CLAUDE.md
They hold the general traits; your job is to make them mine.

Then interview me, one question at a time. No set number of questions —
make each one earn its place, build it on what I've already said, and stop
as soon as another answer wouldn't change what you write. Work out: what I
do day to day, what I want Claude for, how technical I honestly am, what's
annoyed me about AI before, how I like information, and anything you should
always or never do. If I say "just set it up", stop asking and use sensible
assumptions — flag them at the end. If it would genuinely help, research
how people in my line of work get the most out of AI before writing
anything.

Then set up my files:
- The main one at ~/.claude/CLAUDE.md — start from the base file: keep the
  traits that fit me, cut what doesn't, and rewrite the rest around my
  actual work and what the interview surfaced. Leave out the base file's
  last section ("Make this file mine") — it exists for people who skip
  this interview, and you're doing that job now. If I already have a file
  there, merge — never overwrite. Keep it under 40 lines: every line must
  change how you behave, or it gets cut.
- If a specific piece of work came up (a report, a client project,
  something I'm building), also write the file for that work's folder: what
  it is, who it's for, the standards, the things that must never happen.

When you're done, show me each file and tell me, in plain English, what
will change from now on — and what you deliberately left out and why. Then
suggest one small thing to try right now that would have gone differently
before these files existed, so I can see them working.
```

(The same prompt lives in [non-technical/BUILD-PROMPT.md](non-technical/BUILD-PROMPT.md).)

If you only ever use the Claude app rather than Claude Code, copy the contents of [non-technical/CLAUDE.md](non-technical/CLAUDE.md) into Settings → personal preferences — slightly weaker, same idea.

The full plain-English guide: [oliwoodman.com/claude-code/claude-md-non-technical](https://www.oliwoodman.com/claude-code/claude-md-non-technical).

## How these were written

In July 2026, Claude Fable 5 — Anthropic's frontier model — spent its final weekend included on the standard plans. Before the window closed, I had it research Anthropic's own best-practice documentation and the strongest community practice, and then write these templates itself.

That was the whole point of the exercise: you can't keep the model, but you can keep its way of thinking. Whatever a smarter model writes into these files, every future session follows — whichever model it's running on.

The full guide lives at [oliwoodman.com/claude-code/claude-md](https://www.oliwoodman.com/claude-code/claude-md).

## Install (no terminal needed)

Open Claude Code in your project — or a Claude chat with the project connected — and paste this:

```
Please set up my CLAUDE.md files from this repo:
https://github.com/oliwoodman/claude-md-templates

Grab the three templates (computer, project, folder). Put the computer one at
~/.claude/CLAUDE.md and the project one at this project's root. If I already
have a file in either place, merge — don't overwrite. Fill in the bracketed
placeholders by looking through this project and asking me questions where you
can't infer the answer. Skip the folder template unless a subfolder of this
project genuinely needs its own rules. Then show me what you set up.
```

Prefer to do it by hand? Copy each template to its path in the table above.

## Then make them yours

The templates are deliberately generic — the brackets are the point. Don't fill them in by hand. Once the files are in place, hand Claude this:

```
I've just added CLAUDE.md template files (computer level and project level,
maybe a folder one too). Make them mine:

1. Read them, then read this project: the code, the structure, the README.
2. Fill in every bracketed placeholder from what you find. Where you can't
   infer the answer, ask me — one question at a time.
3. Cut any line that doesn't match how I actually work, and add the gotchas
   you can see in this project that the templates miss.
4. Keep every rule at the right tier — computer level for things true
   everywhere, project level for this build, folder level only if a subfolder
   genuinely needs its own rules. Never repeat a rule across tiers.

Show me the final files before saving them, with a short note on what you
changed and why.
```

## The better move: have the smartest model write yours

The templates are good starting points. The real play is [DISTILL-PROMPT.md](DISTILL-PROMPT.md) — a prompt that has Claude dig through your project, interview you about how you work, and write all three tiers from scratch. Run it with the smartest model you have access to.

## The rules that make these files work

- **Specific beats vague.** "Use 2-space indentation" gets followed; "format code properly" gets ignored. If a rule could mean two things, it's not a rule yet.
- **Short files get obeyed, long files get skimmed.** Every line is read every session and costs context. Keep each file under 200 lines. The test per line: would Claude get something wrong without it? If not, delete it.
- **Never repeat a rule across tiers.** The tiers add together; contradictions get resolved arbitrarily.
- **Treat them like a garden.** Claude makes the same mistake twice — add a rule. It already does something without being told — delete that line.

## Pairs well with

[claude-md-coding-guidelines](https://github.com/oliwoodman/claude-md-coding-guidelines) — four rules built from Andrej Karpathy's notes on where AI coding goes wrong. Drops straight into the project tier.

---

Built from Anthropic's [Claude Code best practices](https://code.claude.com/docs/en/best-practices) and [memory documentation](https://code.claude.com/docs/en/memory), plus community practice. Not affiliated with Anthropic.

I post daily about building real things with AI — [@buildwitholi](https://instagram.com/buildwitholi).
