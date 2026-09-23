# Merge, Rebase and Cherry-pick — Full Lecture

### Merge
Combines two lines of development while preserving their existing ancestry.

### Rebase
Replays commits on another base and creates new commit identities.

### Cherry-pick
Applies the change introduced by selected commits onto the current branch.

```bash
git merge feature/x
git rebase main
git cherry-pick <sha>
```

Conflict workflow:
```bash
git status
# edit conflict markers
git add <resolved-files>
git merge --continue   # or git commit for a merge
```

Abort when appropriate with `git merge --abort` or `git rebase --abort`.