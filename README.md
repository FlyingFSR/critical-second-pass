# Critical Second Pass

A Codex skill for doing a harder second read of something already produced:
a proposal, plan, diff, handoff, article, script, or draft.

The skill is intentionally small. It is not a generic review checklist and it
does not force new findings. Its main job is to recover an outside view after a
first pass, then say plainly whether anything material still needs to change.

## When to use it

Use this skill when you explicitly want a second look, such as:

- "pressure-test this"
- "review this again"
- "poke holes in this plan"
- "what risks am I missing?"
- "did we miss anything?"
- "再 review 一遍"
- "挑挑刺"
- "看看有没有风险/遗漏"

Do not use it for ordinary first-pass feedback or casual "what do you think?"
requests.

## Install

Clone or copy this repository into your Codex skills directory:

```bash
mkdir -p "$HOME/.codex/skills"
git clone https://github.com/FlyingFSR/critical-second-pass.git \
  "$HOME/.codex/skills/critical-second-pass"
```

If you are installing from a local checkout instead:

```bash
mkdir -p "$HOME/.codex/skills"
cp -R /path/to/critical-second-pass "$HOME/.codex/skills/critical-second-pass"
```

Restart Codex after installation so the skill metadata is discovered.

## Files

- `SKILL.md` - the actual skill instructions and trigger metadata
- `agents/openai.yaml` - optional Codex UI metadata
- `LICENSE` - MIT license

## Design notes

The skill has three deliberately sharp behaviors:

1. Open with one verdict: `No material changes needed`, `Small refinements`, or
   `Needs correction before proceeding`.
2. Separate consequential findings from optional polish.
3. Say `No material changes needed` when that is the honest answer.

That last point matters. A second pass is useful only if it is allowed to
converge instead of inventing issues to justify itself.

## Related projects

Other open-source tools by the same author:

- [conversation-archive](https://github.com/FlyingFSR/conversation-archive) — a
  skill for AI assistants that turns conversations into structured archives that
  keep their texture, not just their text.
- [Friday](https://github.com/FlyingFSR/friday) — local-first, on-device voice
  input for macOS (whisper.cpp, no cloud).
