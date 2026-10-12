# git stash: save work without committing

**Date:** 2026-10-12
**Tags:** git, workflow

## What I learned

`git stash` puts your uncommitted changes aside so you can switch branches with a clean working tree, then bring the changes back later.

## Example

```
git stash                 # save changes
git stash list            # see saved stashes
git stash pop             # restore the latest stash and remove it
git stash apply           # restore but keep it in the stash list
git stash push -m "wip login form"   # stash with a name
```

By default untracked files are not stashed. Add `-u` to include them.

## Why it matters

Handy when you need to quickly fix something on another branch in the middle of unfinished work.
