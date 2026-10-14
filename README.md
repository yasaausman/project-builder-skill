# project-builder

A Claude Code skill (plus a portable paste-in prompt) that takes a raw idea to a
validated, well-built project — brainstorm, market/feasibility research with a
go/no-go verdict, then an MVP build plan and the actual build.

It produces two files per project:
- **`PLAN.md`** — the decisions (research verdict, MVP scope, pinned stack, milestone checklist).
- **`PROJECT.md`** — the living state, so progress carries across chats.

Every build is held to a **quality bar** (value obvious in 5 seconds, core tech load-bearing,
reproducible proof, narrow-and-deep scope, docs/demo as first-class, polish + personality),
with an extra **hackathon layer** (aim at the center of theme + sponsor purpose + rubric).

## What's here
- `SKILL.md` — the Claude Code skill (three modes: Ideate / Research / Build).
- `project-builder.md` — the portable paste-in version for claude.ai web or any LLM chat.
- `LESSONS.md` — cross-project lessons the skill reads before each mode and writes to when
  something goes wrong, an estimate misses, a verdict proves wrong, or you correct it.
- `PROFILE.md` — your skills, preferred stacks, time and goals, so it stops re-asking.
- `LESSONS.example.md`, `PROFILE.example.md`: blank templates. On first use the skill copies them
  to `LESSONS.md` and `PROFILE.md`, which are git-ignored so updates never clash with your data.
- `references/`: the full quality bar and hackathon layer, loaded when needed.

## Memory across projects
The skill reads `PROFILE.md` and `LESSONS.md` at the start of every mode and applies relevant
lessons (it says so when one changes a recommendation). It logs new lessons as they happen and
runs a short retro when a project wraps or is abandoned. When the same lesson shows up twice, it
proposes a patch to `SKILL.md` and waits for your approval before changing it. The portable
prompt has no memory; it can't write files between chats.

## Install (as a Claude Code skill)
Clone into your personal skills folder:

```bash
git clone https://github.com/yasaausman/project-builder-skill ~/.claude/skills/project-builder
```

Then start a new Claude Code session and run `/project-builder`, or just describe a new
project idea and it triggers automatically.

## Use the portable prompt
Copy the contents of `project-builder.md` into any LLM chat, replace `[YOUR IDEA HERE]`,
and send. Runs research first, stops for your go-ahead, then builds.

## Resuming a project
Save the generated `PROJECT.md` in your repo. Next session, paste it back (or say
"continue" in Claude Code) to pick up exactly where you left off.

## License
MIT
