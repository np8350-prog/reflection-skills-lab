# Lab Proof — Reflection Skills

## Skills installed

- `.agents/skills/post-task-retro/SKILL.md`
- `.agents/skills/error-autopsy/SKILL.md`
- `.agents/skills/weekly-skill-review/SKILL.md`

## Trigger tuning

Each description was written to fire on the situation, not just the exact skill name — post-task-retro triggers on "just finished" or "wrapped up" even without the word "retro", error-autopsy triggers on any broken/failing description even without the word "bug", and weekly-skill-review triggers on requests to turn scattered notes into a focus, not only the phrase "weekly review".

## Sample outputs

### post-task-retro

Input: "Just finished setting up the folder tree and GitHub repo for this lab."

Output:
Goal: Set up the lab's folder structure and GitHub repository.
What worked: The project foundation is now organized and version-controlled.
What snagged: No specific friction point was identified.
Next time: Document setup commands while creating the repository.

### error-autopsy

Input: "My git clone command failed earlier with 'not a git command' error, and I couldn't figure out why at first."

Output:
Symptom: Git reported that the clone subcommand was not a Git command.
Hypothesis: The original command misspelled clone or included a stray character.
Check: Run git clone --help; if it works, Git recognizes the correct subcommand.
Root cause: Most likely malformed input, not a Git installation problem.
Fix: Retype git clone <repository-url> manually.

### weekly-skill-review

Input: three entries — one retro, one error autopsy, one retro with a file-content mistake.

Output:
Themes noticed: Command accuracy, clean pasting, and verification.
Repeated most: Input mistakes caused both Git and file-content problems.
Next week's focus: Verify commands and inspect files immediately after every paste.
Why this one: A quick check prevents small input errors from becoming debugging work.

## Insight

The weekly-skill-review skill only becomes useful once there are at least two or three entries to compare. A single retro or error has nothing to cluster against.
