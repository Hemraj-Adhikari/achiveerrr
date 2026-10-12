# Undoing the last commit

**Date:** 2026-10-12
**Tags:** git, undo

## What I learned

Pick the command based on what you want to keep and whether the commit is already pushed.

## Example

```
# Undo the commit, keep the changes staged
git reset --soft HEAD~1

# Undo the commit, keep the changes unstaged
git reset HEAD~1

# Undo the commit AND throw away the changes (careful)
git reset --hard HEAD~1

# Already pushed? Make a new commit that reverses it
git revert HEAD
```

## Why it matters

`reset` rewrites history, so only use it on commits nobody else has pulled. `revert` is the safe choice for shared branches.
