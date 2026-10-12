# .gitignore does not remove files already tracked

**Date:** 2026-10-12
**Tags:** git, security, secrets

## What I learned

Adding a file to `.gitignore` only stops Git from tracking new files. If a file such as `.env` was already committed, Git keeps tracking it until you remove it from the index.

## Example

```
echo ".env" >> .gitignore
git rm --cached .env
git commit -m "Stop tracking .env"
```

## Why it matters

The file stays in the old commit history. If a real key or password was committed, treat it as leaked: rotate it (generate a new one) instead of just deleting the file.
