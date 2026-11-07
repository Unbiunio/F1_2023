# Command Log

This document tracks Git and SQL commands introduced during the project. Commands are marked as suggested until their execution is confirmed.

## Review cadence

- Count days on which we actively work on the project.
- Review the Git and SQL commands after every three work days.
- Current count: day 2.
- Next review: after day 3 of project work.

## Git

| Date | Command | Purpose | Status |
|---|---|---|---|
| 2026-11-07 | `git init -b main` | Initialize the local repository with `main` as its initial branch. | Executed; confirmed on `main` |
| 2026-11-07 | `git status --short` | Show concise repository status and pending changes. | Executed; four untracked project files listed |
| 2026-11-07 | `git branch --show-current` | Show the current branch name. | Executed; output: `main` |
| 2026-11-07 | `git add .gitignore COMMANDS.md PROGRESS.md PROJECT_F1_2023.md` | Stage only the reviewed project and learning-log files for the first commit. | Executed; all four files staged |
| 2026-11-07 | `git diff --cached` | Review staged changes before committing. | Executed; opened Git's pager, exited with `q` |
| 2026-11-07 | `git status --short` | Confirm exactly which files are staged. | Executed; four intended files staged |
| 2026-11-07 | `git --no-pager diff --cached --stat` | Summarize staged changes without opening a pager. | Executed; four files, 441 insertions |
| 2026-11-07 | `git add COMMANDS.md PROGRESS.md` | Stage the latest updates to the learning logs before the first commit. | Suggested; not executed |
| 2026-11-07 | `git --no-pager diff --cached --stat` | Summarize all staged changes before committing. | Suggested; not executed |
| 2026-11-07 | `git status --short` | Confirm staged files and ensure there are no unstaged changes. | Suggested; not executed |
| 2026-11-07 | `git commit -m "Initial project setup"` | Create the first local commit with the staged project files. | Suggested; not executed |

## SQL

No SQL commands introduced yet.
