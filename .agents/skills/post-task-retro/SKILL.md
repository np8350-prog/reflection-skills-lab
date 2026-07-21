---
name: post-task-retro
description: Use after finishing a task, feature, or piece of work when the user wants a quick learning retro. Triggers on phrases like "just finished", "wrapped up", "done with this", or a direct request to reflect — not only the word "retro". Keep it short, one retro per task.
---

# Post-Task Retro

Run this right after a task is done. Output is always 4 lines, no more.

## Steps

1. Ask what the task was, if not already clear from context.
2. Write exactly 4 lines:
   - **Goal**: what you set out to do, one line.
   - **What worked**: one concrete thing that went well.
   - **What snagged**: one concrete friction point or mistake.
   - **Next time**: one specific change for the next similar task.
3. Keep each line under 20 words. No filler, no praise padding.
4. Do not turn this into a full report. If the user wants more depth, that's a different skill.
5. Append the output to `~/reflection-log.md`, under a new dated heading, above the existing entries (most recent first). Include which repo or lab this came from.

## Output format

### [date] — [repo/lab name]
Goal: ...
What worked: ...
What snagged: ...
Next time: ...
