# Learning Progress

## Current status

- Project: F1 2023 — Alonso vs Verstappen Analytics
- Current phase: Phase 1 — environment setup
- Project work day: 2
- Git repository: local `main` has three commits; `origin` uses HTTPS; remote appears empty; author `Rafa Serichol` and numeric GitHub noreply format verified locally; user chose to save pending logs in a fourth commit; push remains paused
- Python environment: `.venv` created and activated with Python 3.12.10; VS Code interpreter verified

## Completed

- Confirmed Python 3.12.10 and Python 3.13.9 are available.
- Confirmed Git is installed.
- Created and activated `.venv` using Python 3.12.10.
- Confirmed VS Code uses the virtual environment.
- Added `.gitignore` entries for `AGENTS.md`, `.venv/`, `__pycache__/`, and `*.py[cod]`.
- Initialized the local Git repository on `main`.
- Created the first local commit (`8e969b2`, `Initial project setup`) with the four intended files.
- Verified the commit contents and confirmed the working tree was clean immediately afterward.
- Created the second local commit (`0036587`, message `Document Github Septup`) and third local commit (`e72fafa`, `Document GitHub remote setup`).
- Configured `origin` as `https://github.com/Unbiunio/F1_2023.git` and verified HTTPS for fetch and push.
- Checked the remote with `git ls-remote origin HEAD`; it returned no output, consistent with an empty repository.
- Verified the current branch is `main` and the working tree is clean.
- Git reported that the commit author identity was selected automatically. User chose to pause and review/configure another identity before publishing.
- Inspected all three local commits: they use the same automatically selected identity, including an email with a work-looking domain. Do not publish this history without an explicit decision.
- User chose to use a GitHub `noreply` address for public commits.
- Screenshot confirms GitHub displays a `noreply` address; the "Keep my email addresses private" setting is currently off. Address intentionally not copied into project docs.
- User selected `Rafa Serichol` as the visible author name and authorized rewriting the three local, unpublished commits. This changes their hashes but not project file contents.
- Verified the repository-local author name and confirmed the configured email matches GitHub's numeric `users.noreply.github.com` format, without printing it.
- `COMMANDS.md` and `PROGRESS.md` have documentation updates not yet committed, so the worktree is not clean.
- User chose to correct the email and save the pending learning-log updates in a fourth local commit.
- The screenshot showed GitHub's "Keep my email addresses private" setting off; user has not yet confirmed changing it.

## Python

- Practiced: choosing a Python interpreter, creating a virtual environment, and activating it in Git Bash.
- Difficulties: none reported so far.
- Next: continue with a small environment check after local Git setup.

## SQL

- Practiced: no SQL commands yet.
- Difficulties: not assessed.
- Next: introduce SQL alongside early data exploration, without installing packages before discussing them.

## Git

- Practiced: checked the Git version.
- Practiced: `git init -b main`, `git status --short`, `git branch --show-current`, `git add`, and `git diff --cached`.
- Learned: Git's diff may open a pager; pressing `q` exits it. `--no-pager` shows command output directly.
- Checked `git config --show-origin --get user.name`; it returned no output, so no explicit author name is configured in the checked Git config.
- Checked `git config --show-origin --get user.email`; it returned no output, so no explicit author email is configured in the checked Git config.
- Do not publish the current author identity without an explicit decision.
- Next: enable "Keep my email addresses private" in GitHub Settings → Emails if not already done. Stage and commit pending logs as a fourth commit. Then confirm whether the authorized rewrite should include all four commits; do not push yet.

## Next exercise

Three local commits are complete. The repository-local author name and numeric GitHub noreply format are verified. The user chose a fourth commit to preserve pending logs. Ensure GitHub email privacy is enabled, commit the logs, confirm rewrite scope, and keep push paused until the rewritten history is verified.
