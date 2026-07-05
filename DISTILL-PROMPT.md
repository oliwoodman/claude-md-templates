# The Distill Prompt

Run this with the smartest model you have access to, in Claude Code at your project's root (or a chat with the project connected). It writes your three tiers for you — and what it writes down, you keep, whichever model you're on next.

```
I want you to write my CLAUDE.md files — the standing instructions every future
session will follow.

1. First, look through this project: the code, the structure, the README, and
   any existing CLAUDE.md files.
2. Then interview me: ask up to 8 questions, one at a time, about how I like to
   work, what keeps going wrong, how technical I am, and anything you can't
   infer from the code.
3. Then write three files:
   - ~/.claude/CLAUDE.md (computer level): only things true for every project
     I'll ever work on.
   - CLAUDE.md at this project's root: only things specific to this project —
     what it is, stack, commands, structure, conventions, gotchas.
   - If any subfolder genuinely has different rules, a short CLAUDE.md for that
     folder.

Rules for writing them: be specific, never vague ("use 2-space indentation",
not "format code properly"). Keep each file well under 200 lines — shorter is
better. Include only instructions I'd otherwise have to keep repeating —
nothing you can infer from the code itself. Never repeat a rule across two
tiers. Where a rule isn't self-evident, add its one-line reason. Every line
has to earn its place.

Show me each file before saving it, and tell me what you deliberately left out
and why.
```
