# Learning Progress

## Current status

- Project: F1 2023 — Alonso vs Verstappen Analytics
- Current phase: Phase 1 — environment setup
- Project work day: 2
- Git repository: local `main` has commits `8e969b2` and `0036587`; `origin` now points to HTTPS; remote appears empty and has not received a push
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
- Created the second local commit (`0036587`); verified the working tree is clean and no remote is configured.
- Configured `origin` as `https://github.com/Unbiunio/F1_2023.git` and verified HTTPS for fetch and push.
- Checked the remote with `git ls-remote origin HEAD`; it returned no output, consistent with an empty repository.
- Latest log changes are uncommitted; stage and commit them before pushing.

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
- Next: commit the latest GitHub setup notes, then push the local `main` branch.

## Next exercise

Two local commits are complete. `origin` is configured with HTTPS, and the remote appears empty. Commit the latest setup notes and then push `main`; nothing has been published yet.
