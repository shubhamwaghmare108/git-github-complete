# History and Inspection — Full Lecture

Useful views:
```bash
git log --oneline
git log --graph --decorate --all
git show HEAD
git show --stat HEAD
git diff HEAD~1 HEAD
git blame <file>
git reflog
```

### Commit ranges
`A..B` asks which commits are reachable from B but not A. `A...B` describes the symmetric difference and is useful for comparing branches.

### Bisect
`git bisect` performs a binary search through history to identify the first bad commit.

```bash
git bisect start
git bisect bad
git bisect good <known-good>
# test each checkout
git bisect good   # or bad
git bisect reset
```
