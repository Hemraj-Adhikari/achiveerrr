# Feature branch workflow

**Date:** 2026-10-12
**Tags:** git, github, workflow

## What I learned

Never work directly on `main`. Create a branch per change, push it, open a pull request, review it, then merge.

## Example

```
git checkout main
git pull
git checkout -b feature/login-fix
# make changes
git add .
git commit -m "Fix login redirect"
git push -u origin feature/login-fix
```

Then open a PR on GitHub and merge it.

## Why it matters

`main` stays stable, every change has a history, and it is easy to review or undo a single change.
