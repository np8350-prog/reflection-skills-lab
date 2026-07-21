# How This Went — From Lab to Real System

## 1. Built the lab structure
Created the repo, three empty folders under `.agents/skills/`.

## 2. Wrote three skills
post-task-retro, error-autopsy, weekly-skill-review — each as a proper SKILL.md with frontmatter and steps.

## 3. Tested with explicit trigger
Ran each with `$skill-name` to confirm the format worked.

## 4. Wrote lab_proof.md
Linked the three skills, showed sample output, made it the entry point for a reviewer.

## 5. Pushed everything, submitted
Lab was technically done at this point.

## 6. Asked "how do I test this in real life"
That's when the real gap showed up: explicit `$skill-name` always works, it proves nothing. The real test is implicit triggering — does Codex pick the skill on its own from normal language, no `$`.

## 7. Found problem one: scope
Skills only lived in this repo (REPO scope). Wouldn't work in any other lab's folder. Fixed by copying them to `~/.agents/skills` (USER scope), works everywhere now.

## 8. Found problem two: no memory
Even with USER scope, each skill run only sees what's typed into that one message. Nothing carries over between sessions or repos. weekly-skill-review had nothing real to review.

## 9. Fixed memory
Created one file, `~/reflection-log.md`, living outside any repo. Updated post-task-retro and error-autopsy to append their output there. Updated weekly-skill-review to read from it instead of needing entries pasted in by hand.

## 10. Synced and pushed
Copied the updated SKILL.md files to USER scope so both copies match. Committed and pushed the repo copies to GitHub.

## Where it ended up
Three skills that work in any repo, write to one shared log, and weekly-skill-review can pull real cross-repo history instead of staged examples. Started as a lab exercise, ended as a working system.
