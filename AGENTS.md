# AGENTS.md

Instructions for AI agents (Claude Code, Codex, Cursor, Copilot, etc.) working in this repository. These rules mirror the human rules in [README.md](README.md) and are mandatory.

## 1. Identify whose session this is

Before changing anything, determine the GitHub username of the person you are working for:

```bash
gh api user --jq .login        # preferred
git config user.name           # fallback
```

If you cannot determine it with confidence, **ask the user**. Do not guess.

## 2. Where you may write

| Path | Pssumu (repo owner) | Any other member |
|---|---|---|
| `members/<own username>/` | edit | edit |
| `members/<someone else>/` | read only | **read only** |
| `plans-and-ideas/` | edit | read only |
| `references/` | edit | read only |
| Root files (`README.md`, `AGENTS.md`, `CLAUDE.md`, `.gitignore`, `.github/`) | edit | read only |

"Read only" means you may open, read, copy from, and download those files, but you must not create, modify, rename, move, or delete anything there — not even formatting fixes.

If the user asks for a change outside their allowed paths:
- Explain this rule and decline that part.
- Offer to put the new or changed version in their own `members/<username>/` folder instead (copy first, then edit the copy).

## 3. Before you commit or push

1. `git pull` first.
2. Check what you are about to commit:
   ```bash
   git status --short
   git diff --cached --name-status
   ```
   Every path must be inside the user's allowed paths from section 2. If anything else is staged, unstage it (`git restore --staged <path>`) and tell the user.
3. Prefer staging only the user's folder: `git add members/<username>/`. Avoid `git add -A` / `git add .` unless you have checked the result.
4. Never force push (`git push --force`), never rewrite published history, and never delete `main`. The `main` branch is protected against both.
5. Write a clear commit message describing what changed.

## 4. Other rules

- Do not change repository settings, collaborators, branch rules, or visibility. Only the owner (Pssumu) manages these, in the GitHub web UI.
- Do not commit secrets, passwords, API keys, or personal data. This repository is **public**.
- Keep files under 50 MB (GitHub rejects files over 100 MB). Ask before adding large datasets.
- Do not commit OS or editor junk (`.DS_Store`, Office lock files `~$*`); `.gitignore` already covers these.
- Binary files (Word, PDF) cannot be merged. Do not overwrite a file someone else may be editing.
