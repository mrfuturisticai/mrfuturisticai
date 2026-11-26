---
name: project-vault
description: Retrieve prior project context, inspect the matching GitHub repository, continue implementation, and keep project documentation and status current.
---

# Project Vault Skill

## When to use
Use this workflow whenever Riyas asks to start, continue, fix, review, document, package, or publish one of his projects.

## Required workflow
1. Identify the project from the request and conversation context. Do not ask Riyas to repeat details already available.
2. Retrieve relevant prior project context before planning. Use the current conversation first; when prior decisions or missing details matter, search available personal context.
3. Read `PROJECT_INDEX.md` and inspect the matching GitHub repository before changing code.
4. Check the repository's README, instructions, current branch, recent commits, and relevant files. Treat GitHub as the source of truth for committed project code.
5. Give a short execution plan only when useful. Then do the work. Ask one question only if a missing decision blocks safe progress.
6. Preserve existing architecture, working features, secrets, user data, and unrelated files. Never commit API keys, passwords, tokens, private customer data, or `.env` files.
7. Verify changes with available tests, checks, or direct inspection. Report what was actually verified and what remains unverified.
8. Update the project's README and `PROJECT_INDEX.md` with truthful status, architecture, setup, verification, and next steps.
9. Commit or upload to GitHub only when the user has authorized repository changes for the task. Never claim a push, deployment, or sync unless the tool confirms it.
10. Keep responses short: state the result, verification, and next action. Prefer doing over explaining.

## Status vocabulary
Use only these labels:
- `Planned`: idea or requirements only.
- `In progress`: implementation has started but is incomplete.
- `Prototype`: a working or partially working demonstration, not production-ready.
- `Verified`: the stated functionality passed a specific check.
- `Deployed`: a live deployment was confirmed.
- `Archived`: intentionally retained but not actively developed.

Do not describe an architecture, prompt, or design as a completed deployed product.

## GitHub safety
- Inspect before editing.
- Never overwrite or delete files without checking their current contents and obtaining approval when the change is destructive or broad.
- Prefer small, reviewable commits.
- Keep credentials in secure secret storage; commit only example placeholders such as `.env.example`.
- Do not move private Career OS or family-app material into public repositories.
- Keep unrelated client/demo data separate.
