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
| 2026-11-07 | `git add COMMANDS.md PROGRESS.md` | Stage the latest updates to the learning logs before the first commit. | Executed |
| 2026-11-07 | `git --no-pager diff --cached --stat` | Summarize all staged changes before committing. | Executed |
| 2026-11-07 | `git status --short` | Confirm staged files and ensure there are no unstaged changes. | Executed before commit |
| 2026-11-07 | `git commit -m "Initial project setup"` | Create the first local commit with the staged project files. | Executed; commit `8e969b2` |
| 2026-11-07 | `git log -1 --oneline` | Verify the latest commit. | Executed; confirmed `8e969b2` |
| 2026-11-07 | `git show --stat --oneline --summary HEAD` | Review files and summary in the latest commit. | Executed; four intended files committed |
| 2026-11-07 | `git status --short` | Check for remaining uncommitted changes. | Executed; clean at verification time |
| 2026-11-07 | `git remote -v` | List configured remote repositories. | Executed; no remote configured |
| 2026-11-07 | `git add COMMANDS.md PROGRESS.md` | Stage the latest GitHub setup and learning progress notes. | Executed |
| 2026-11-07 | `git --no-pager diff --cached --stat` | Summarize staged documentation changes before committing. | Executed |
| 2026-11-07 | `git status --short` | Confirm the intended files are staged and no other changes are pending. | Executed; only two log files staged |
| 2026-11-07 | `git commit -m "Document Github Septup"` | Save the updated logs in a second local commit. | Executed; commit `0036587` |
| 2026-11-07 | `git log -2 --oneline` | Verify the two latest commits. | Executed; latest was `0036587` |
| 2026-11-07 | `git status --short` | Check for uncommitted changes. | Executed; clean at verification time |
| 2026-11-07 | `git remote -v` | List configured remote repositories. | Executed; verified HTTPS fetch/push URL |
| 2026-11-07 | `git remote add origin http://github.com/Unbiunio/F1_2023.git` | Add the GitHub remote. | Executed; initially configured as HTTP |
| 2026-11-07 | `git remote set-url origin https://github.com/Unbiunio/F1_2023.git` | Set the remote URL to HTTPS. | Executed |
| 2026-11-07 | `git add COMMANDS.md PROGRESS.md` | Stage the latest GitHub setup and learning progress notes. | Executed |
| 2026-11-07 | `git --no-pager diff --cached --stat` | Summarize staged documentation changes before committing. | Executed |
| 2026-11-07 | `git status --short` | Confirm only the intended log files are staged. | Executed; only two log files staged |
| 2026-11-07 | `git commit -m "Document GitHub remote setup"` | Save the latest remote setup notes in a local commit. | Executed; commit `e72fafa` |
| 2026-11-07 | `git log -3 --format="%h %s"` | Verify the latest three commits. | Executed; latest is `e72fafa` |
| 2026-11-07 | `git branch --show-current` | Verify the current branch before publishing. | Executed; `main` |
| 2026-11-07 | `git ls-remote origin HEAD` | Check whether the remote has a HEAD commit. | Executed; no output, consistent with an empty remote |
| 2026-11-07 | `git status --short` | Check for uncommitted changes. | Executed; clean at verification time |
| 2026-11-07 | `git push -u origin main` | Publish the `main` branch to GitHub and set its upstream. | Paused; do not run until author identity is reviewed |
| 2026-11-07 | `git config --show-origin --get user.name` | Inspect the configured Git author name and where it is set. | Executed; no output, so no explicit `user.name` was found in the checked configuration |
| 2026-11-07 | `git config --show-origin --get user.email` | Inspect the configured Git author email and where it is set. | Executed; no output, so no explicit `user.email` was found in the checked configuration |
| 2026-11-07 | `git log -3 --format="%h %an <%ae>"` | Inspect author names and emails recorded in the latest three local commits. | Executed; all three have the same automatically selected identity |
| 2026-11-07 | `git config user.name "Rafa Serichol"` | Set the author name for this repository. | Executed; verified locally |
| 2026-11-07 | `git config user.email "TU_DIRECCION_NOREPLY"` | Set the author email for this repository to the exact address shown in GitHub Settings → Emails. | Executed; expected numeric GitHub noreply format verified without printing the address |
| 2026-11-07 | `git config --local --get user.name` | Verify the repository-local author name. | Executed; `Rafa Serichol` |
| 2026-11-07 | `git config --local --get user.email` | Verify the repository-local author email. | Verified without exposing it; matches numeric `users.noreply.github.com` format |
| 2026-11-07 | `git config user.email "TU_DIRECCION_NOREPLY"` | Correct the repository-local email using the exact address in GitHub Settings → Emails. | Executed |
| 2026-11-07 | Noreply format check | Check the configured email format without printing the address. | Executed; valid numeric GitHub noreply format |
| 2026-11-07 | `git add COMMANDS.md PROGRESS.md` | Stage the pending learning-log updates. | Suggested; not executed |
| 2026-11-07 | `git --no-pager diff --cached --stat` | Summarize staged learning-log changes before committing. | Suggested; not executed |
| 2026-11-07 | `git status --short` | Confirm only the intended log files are staged. | Suggested; not executed |
| 2026-11-07 | `git commit -m "Document author privacy setup"` | Save the learning-log updates in a fourth local commit. | Suggested; not executed |
| 2026-11-07 | `git rebase --root --exec "git commit --amend --no-edit --reset-author"` | Rewrite local commits from the root using the configured author identity. | User authorized rewriting the first three; confirm whether to include the new fourth commit before running |

## SQL

No SQL commands introduced yet.
