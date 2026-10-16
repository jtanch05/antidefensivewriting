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

## Practical examples

These examples show the kinds of edits the skill makes. Numerical examples are illustrative; use your own verified results.

### 1. Make compressed slide text understandable

**Before:** “Node/base methods changed together; runtime unchanged.”

**After:** “Both neighbour and base-station methods changed between versions. Overall runtime remained similar.”

The revision explains the relationship without requiring the audience to decode shorthand.

```text
$antidefensivewriting Improve this slide for classmates who have not seen the code. Keep it concise, explain ambiguous shorthand, and preserve the technical meaning.
```

### 2. Match a performance claim to the measurement

**Evidence supplied:** Neighbour-query time fell by 30%; total execution time remained similar.

**Before:** “The optimised program is 30% faster.”

**After:** “The optimisation reduced neighbour-query time by 30%. Total execution time remained similar.”

The claim now describes the measured improvement without extending it to the whole program.

### 3. State a limitation without defensive writing

**Before:** “Although we unfortunately could not test every configuration, we believe our implementation is still robust and reliable.”

**After:** “The implementation passed the tested configurations. Behaviour under other configurations has not been verified.”

This removes the apology and unsupported assurance while retaining the limit.

### 4. Turn generic report prose into an explanation

**Evidence supplied:** A system sends each update to every node, so adding nodes increases the number of recipients per update.

**Before:** “Scalability is an important consideration for this system.”

**After:** “Each update is sent to every node, so adding nodes increases the communication work per update. This may limit scalability as the system grows.”

The revision connects the design to its likely consequence. It does not claim that a bottleneck was measured.

```text
$antidefensivewriting Review this discussion paragraph. Identify claims that need evidence or explanation, then revise using only the supplied results. Ask before filling any material evidence gap.
```

### 5. Handle missing evidence without inventing a conclusion

**Draft:** “Method B is more accurate than Method A.”

**Available material:** A description of both methods, with no accuracy results.

**Useful response:** Ask for the evaluation results, accuracy metric, and test conditions before drafting the comparison. Continue editing other passages whose meaning is already supported.

The skill can improve wording immediately, but it cannot establish a missing result through rewriting.

## Core standard

Do not use fluent wording to cover a gap in evidence or reasoning. Important claims should make clear what is being asserted, what supports it, why the evidence matters, and what conclusion or action follows. If a material fact or source is missing, ask the user before drafting that argument.

## Files

- `SKILL.md` contains the main behavior and workflow.
- `references/source-and-evidence-gate.md` handles source conflicts, evidence gaps, and research boundaries when needed.
- `references/reasoning-and-specificity.md` helps repair analytical gaps and vague claims.
- `references/student-voice.md` addresses persistent robotic, compressed, or defensive phrasing.
