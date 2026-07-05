# The Three-Tier CLAUDE.md Templates

Claude reads your CLAUDE.md files before every single prompt — they're its standing orders. Most people know about one, in the project root. There are actually three tiers, and the difference is reach:

| Tier | Lives at | Applies to |
|---|---|---|
| **Computer** | `~/.claude/CLAUDE.md` | Every project you ever open |
| **Project** | `your-project/CLAUDE.md` | This project, every session, shared with your team via git |
| **Folder** | `any-folder/CLAUDE.md` | Just that corner — only loaded when Claude works in there |

The test for where a rule goes: true for everything you build? Computer. True for this project? Project. True for one corner of it? Folder. A rule lives at exactly one tier — the highest one where it's still true — because the files add together, they don't override each other.

This repo holds a starter template for each tier, plus the prompt that gets Claude to write yours properly.

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
