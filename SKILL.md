---
name: critical-second-pass
description: >-
  Use when the user explicitly asks for a second, harder look at something
  already produced: a prior answer, proposal, plan, findings, workflow or
  governance decision, diff, completed change, handoff, or written draft.
  Triggers include "re-review", "review again", "pressure-test this", "poke
  holes", "red-team this", "stress test", "sanity check this", "audit", "what
  risks am I missing", "can this be improved", "did we miss anything", "再
  review 一遍", "二次 review", "再看一遍能不能更好", "挑挑刺", "看看有没有风险/遗漏",
  and "帮我 pressure test 一下". Do not use for casual first-pass feedback such
  as "what do you think?" or "review this" without an explicit second-pass or
  pressure-test intent.
---

# Critical Second Pass

## Goal

Re-examine a prior output as if a different agent produced it, and report
honestly what, if anything, still needs to change.

A second pass is valuable because the first pass is usually written under
momentum and mild confirmation bias. The job is to recover the outside view that
momentum buried. Do not manufacture findings. `No material changes needed` is a
valid and useful result.

## Trigger Boundary

Use this only when the user explicitly asks for a second look, re-review, audit,
pressure test, risk check, improvement check, or whether a prior output can be
improved.

Do not trigger on casual first-pass feedback, ordinary clarification, or a
generic request to review something for the first time. If the intent is
unclear, ask one short clarifying question.

## What To Review

If the user names the artifact, review exactly that. If they do not, default to
the most recent substantive output in the conversation: the last proposal,
finding set, plan, draft, diff, handoff, or completed change.

If several artifacts are plausible, name the one you are reviewing in the first
line so the user can redirect cheaply.

## Modes

Pick the mode that matches the artifact. Some artifacts need both.

**Ops / Decision Mode**

Use for proposals, plans, workflow or governance decisions, diffs, code,
handoffs, and completed implementation work. Test whether the next step will
execute correctly and whether the reasoning holds up.

**Content / Creative Mode**

Use for scripts, articles, posts, essays, and other material meant to be read or
heard. Test whether it is true, whether it lands, and whether it sounds like the
user rather than generic AI writing.

## Priority

Rank by consequence, not cleverness.

- **P1** - would change the decision or outcome if left in.
- **P2** - worth fixing because it reduces risk, confusion, or future rework,
  but the work survives without it.
- **P3** - optional polish.
- **Keep** - working parts that should stay.

For content work, P1 includes false claims, off-voice material that reads as AI,
an opening that does not earn attention, or a privacy/boundary issue.

For ops work, P1 includes stale status, a broken handoff, misleading
verification, wrong ownership, or a recommendation that would cause incorrect
execution.

## Output

Open with exactly one verdict, then the findings:

- `No material changes needed`
- `Small refinements`
- `Needs correction before proceeding`

Then provide findings by priority, followed by the single smallest useful next
action.

Be concise and concrete. Include file references when reviewing files. If
nothing material needs to change, say so clearly and name any residual risk
instead of inventing work.

## Workflow

1. Identify the artifact under review.
2. Inspect current files, diffs, commits, drafts, tests, or logs when they are
   involved. Do not review from memory if the artifact can be checked.
3. Stay in scope. Raise adjacent issues only when they directly affect the
   decision at hand.
4. Give the verdict, findings by priority, and the smallest useful next action.
5. Do not implement changes unless the user explicitly asks you to apply or fix
   them.
6. Do not recursively review your own second pass unless the user asks for
   another round.

## Common Risk Checks

Use only the checks that fit the artifact.

Ops / decision:

- A one-off judgment promoted into a global rule.
- Too much process, documentation, or record-keeping added.
- Stale status, stale handoff instructions, or contradictory source-of-truth
  surfaces.
- A recommendation with no owner, file, action, or decision gate.
- Verification weaker than the confidence claimed.
- A non-problem solved, or the right problem solved at the wrong layer.
- A technically true finding that is not worth acting on.
- A fix that risks undoing user-owned or unrelated work.

Content / creative:

- The agent's framing presented as the user's lived experience.
- An emotional beat or claim that rings false.
- Generic phrasing that reads as AI.
- An opening that does not earn attention.
- A privacy or identity boundary crossed without need.

## Convergence

On repeat passes, if what remains is only P3 or mostly restates earlier points,
say so plainly. Name the residual risk, recommend stopping if that is the right
call, and hand the decision back to the user.
