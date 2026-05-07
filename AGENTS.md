# AGENTS.md

> Operational context for AI coding agents (Claude, Copilot, Cursor, etc.) working in **`nosportugal/flai-workshop-github-copilot-100`**.

## Project Overview

**Getting Started with GitHub Copilot**

<p align="center">

Owner team: **flai-contributores** (org: nosportugal).

## Tech Stack

- Languages: Python
- Package manager(s): pip (requirements.txt)
- CI: GitHub Actions

## Local Development

Common commands you should know before changing this codebase:

```bash
# Create venv and install
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

# Run tests
pytest
```

## Project Structure

- `src/` — main source code

## Conventions

- Default branch is `main`.
- Use [Conventional Commits](https://www.conventionalcommits.org/) for messages: `feat:`, `fix:`, `chore:`, `docs:`, `refactor:`, `test:`.
- Open a Pull Request for review; do not push to the default branch directly when possible.
- Run linters/formatters before committing.
- Keep PRs small and focused.
- Follow PEP 8. Type hints encouraged on public functions.

## CI/CD

- CI is configured under `.github/workflows/`.
- Make sure your changes don't break existing workflow files.

## Security & Secrets

- **Never** commit secrets, tokens, API keys, certificates or credentials.
- Use environment variables, GCP/Azure Secret Manager, or the org's vault.
- If you spot a leaked secret, rotate it immediately and notify the security team.
- Avoid logging PII or customer data in plaintext.

## Guidance for AI Agents

When working in this repository, agents should:

- Read the README and any docs under `docs/` before making non-trivial changes.
- Prefer minimal, surgical edits over rewrites.
- Match the existing code style — do not reformat unrelated code.
- After changes, run the build/test/lint commands listed above and report the result.
- Open a draft PR for any change touching more than one module or > 100 LOC, and let a human review.
- Do not invent commands or dependencies — verify they exist in the repo before suggesting them.
- If unsure about business logic, **ask** rather than guess.

---

_This AGENTS.md was bootstrapped automatically from the repo contents on first creation. Refine it with project-specific details._