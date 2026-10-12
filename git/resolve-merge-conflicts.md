# Resolving a merge conflict

**Date:** 2026-10-12
**Tags:** git, merge

## What I learned

A conflict happens when two branches change the same lines. Git marks the file and waits for you to choose the final content.

## Example

```
<<<<<<< HEAD
my version of the line
=======
their version of the line
>>>>>>> feature-branch
```

Steps:

1. Open the file and edit it to the final version (remove all three marker lines)
2. `git add the-file`
3. `git commit` (or `git merge --continue`)

`git merge --abort` cancels the merge and returns to the state before it.

## Why it matters

Conflicts are normal when several people work on the same project. Small, frequent PRs make them smaller.
