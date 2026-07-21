---
name: error-autopsy
description: Use when something broke — a bug, a failed run, a stack trace, or a vague "this isn't working and I don't know why." Triggers on error messages, crash reports, and unexpected behavior reports. Not for general code review or planning.
---

# Error Autopsy

A fast, reusable way to diagnose a failure. Not an incident report, not a full postmortem.

## Steps

1. State the error or symptom in one line, in plain words.
2. Form one hypothesis for the most likely cause. Just one, the strongest guess.
3. Name the smallest possible check that would confirm or kill that hypothesis (a log line, a single test, a print statement, a config check).
4. If the check fails the hypothesis, form the next hypothesis and repeat step 3. Don't stack multiple hypotheses at once.
5. Once confirmed, write one line: root cause. Then one line: the fix.
6. Append the output to `~/reflection-log.md`, under a new dated heading, above the existing entries (most recent first). Include which repo or lab this came from.

## Output format

### [date] — [repo/lab name]
Symptom: ...
Hypothesis: ...
Check: ...
Root cause: ...
Fix: ...

## Boundaries

- Do not write a long incident writeup. This is a diagnostic pattern, not documentation.
- If the check disproves the hypothesis, show the new hypothesis, don't hide the miss.
