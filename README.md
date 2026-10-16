# Antidefensivewriting

A subject-neutral Codex skill for academic reports, proposals, slide text, and technical explanations with evidence-based reasoning and fluent, clear, professional student-level English.

It addresses defensive explanations, incomplete reasoning, generic claims, robotic prose, and compressed technical shorthand without weakening factual accuracy.

## What it does

- Scales source reading to the task: a wording edit stays focused; a compliance review checks the brief, rubric, template, and relevant evidence.
- Asks focused questions when material evidence is missing; it does not invent facts or silently assume.
- Uses university materials as the authority for course-specific methods and terminology.
- Uses supplied evidence first and asks before outside research unless it is already authorized.
- Connects important claims to evidence, explanation, implications, decisions, and relevant limits.
- Rewrites vague, robotic, compressed, or defensive prose while preserving technical meaning and uncertainty.
- Reviews reports by diagnosing the reasoning gaps before proposing targeted revisions.
- Loads supporting references only when the current task needs them.

## Install

Clone this repository into your Codex skills directory:

```powershell
git clone https://github.com/jtanch05/antidefensivewriting.git "$env:USERPROFILE\.codex\skills\antidefensivewriting"
```

Restart or refresh Codex so it can discover the skill. Invoke it explicitly as `$antidefensivewriting` or let Codex select it for relevant academic writing and review tasks.

## Use

Examples:

```text
$antidefensivewriting Review this report against the assignment rubric. Diagnose issues before rewriting.
```

```text
$antidefensivewriting Help me plan this report. First inspect the specification, rubric, template, and relevant lecture materials; ask me for any important missing evidence before drafting.
```

```text
$antidefensivewriting Rewrite this paragraph in clear undergraduate English. Preserve my meaning and flag any claim that lacks evidence.
```

```text
$antidefensivewriting Make this slide text natural and easy to understand. Preserve the technical terms, evidence, and necessary limitations.
```

## Core standard

Do not use fluent wording to cover a gap in evidence or reasoning. Important claims should make clear what is being asserted, what supports it, why the evidence matters, and what conclusion or action follows. If a material fact or source is missing, ask the user before drafting that argument.

## Files

- `SKILL.md` contains the main behavior and workflow.
- `references/source-and-evidence-gate.md` handles source conflicts, evidence gaps, and research boundaries when needed.
- `references/reasoning-and-specificity.md` helps repair analytical gaps and vague claims.
- `references/student-voice.md` addresses persistent robotic, compressed, or defensive phrasing.
