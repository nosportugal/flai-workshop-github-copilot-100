# AGENTS.md

> Operational context for AI coding agents (Claude, Copilot, Cursor, etc.) working in **`nosportugal/flai-workshop-github-copilot-100`**.

## Project Overview

**Getting Started with GitHub Copilot**

A [GitHub Skills](https://github.com/skills/getting-started-with-github-copilot) exercise used in the NOS flAI workshops: learners use Copilot to improve the Mergington High School activities website in `src/`.

Owner team: **flai-contributors** (org: nosportugal).

## Tech Stack

- Languages: Python (FastAPI backend), JavaScript/HTML/CSS (static frontend)
- Package manager(s): pip (requirements.txt)
- CI: none; GitHub Actions only runs the exercise step workflows

## Local Development

Common commands you should know before changing this codebase:

```bash
# Create venv and install
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

# Run the app on port 8000 (or use the "Launch Mergington WebApp" debug config)
uvicorn src.app:app --reload

# Run tests (pytest and tests/ are only added by the learner in step 4)
pytest
```

## Project Structure

- `src/` — main source code

## Conventions

- Default branch is `main`.
- Use [Conventional Commits](https://www.conventionalcommits.org/) for messages: `feat:`, `fix:`, `chore:`, `docs:`, `refactor:`, `test:`.
- Open a Pull Request for review; do not push to the default branch directly when possible.
- Keep PRs small and focused.
- Follow PEP 8. Type hints encouraged on public functions.

## CI/CD

- `.github/workflows/` holds the exercise workflows (`0-start-exercise.yml`, then `1-step.yml` to `5-step.yml`), which check each step's work and post the next `.github/steps/*.md` file as an issue comment. There is no build or test CI.
- Make sure your changes don't break existing workflow files.

## Security & Secrets

- **Never** commit secrets, tokens, API keys, certificates or credentials.
- Use environment variables, GCP/Azure Secret Manager, or the org's vault.
- If you spot a leaked secret, rotate it immediately and notify the security team.
- Avoid logging PII or customer data in plaintext.

## Guidance for AI Agents

When working in this repository, agents should:

- Read `README.md` and `src/README.md` before making non-trivial changes.
- Prefer minimal, surgical edits over rewrites.
- Match the existing code style — do not reformat unrelated code.
- After changes, run the commands listed above and report the result.
- Let a human review every change. In the exercise, the learner opens the pull request from `accelerate-with-copilot` to `main` in step 5.
- Do not invent commands or dependencies — verify they exist in the repo before suggesting them.
- If unsure about business logic, **ask** rather than guess.

---

_This AGENTS.md was bootstrapped automatically from the repo contents on first creation. Refine it with project-specific details._
