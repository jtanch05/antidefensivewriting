# Antidefensivewriting

A subject-neutral Codex skill for writing and reviewing university reports with clear reasoning, specific evidence, direct prose, and a natural undergraduate voice.

It is designed for reports and proposals across computer science and other university subjects. It focuses on fixing three recurring writing problems: defensive explanations, claims with too little reasoning, and polished but overly general sentences.

## What it does

- Checks assignment requirements, rubrics, templates, relevant university class materials, and the student's own evidence before drafting.
- Asks focused questions when material evidence is missing; it does not invent facts or silently assume.
- Uses university materials as the authority for course-specific methods and terminology.
- Does not browse the web by default. It asks the user before using outside sources.
- Connects important claims to evidence, explanation, implications, decisions, and relevant limits.
- Rewrites vague or defensive prose into direct, clear student-level English while preserving meaning and uncertainty.
- Reviews reports by diagnosing the reasoning gaps before proposing targeted revisions.

## Install

Clone this repository into your Codex skills directory:

```powershell
git clone https://github.com/jtanch05/antidefensivewriting.git "$env:USERPROFILE\.codex\skills\antidefensivewriting"
```

Restart or refresh Codex so it can discover the skill. It can be invoked explicitly as `$antidefensivewriting` and is also available for automatic selection on relevant report-writing and review tasks.

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

## Core standard

Do not use fluent wording to cover a gap in evidence or reasoning. Important claims should make clear what is being asserted, what supports it, why the evidence matters, and what conclusion or action follows. If a material fact or source is missing, ask the user before drafting that argument.

## Files

- `SKILL.md` contains the main behavior and workflow.
- `references/source-and-evidence-gate.md` defines source priority, evidence checks, and when to ask before drafting.
- `references/reasoning-and-specificity.md` provides adaptable reasoning and specificity checks.
- `references/student-voice.md` covers direct, non-defensive university writing.
