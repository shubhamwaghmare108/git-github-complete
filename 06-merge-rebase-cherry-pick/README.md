# 06 — Merge, Rebase and Cherry-pick

### Merge
Combines histories and may create a merge commit.

### Rebase
Replays commits on a new base and rewrites commit identities.

```bash
git merge feature/login
git rebase main
git cherry-pick <commit>
```

Do not casually rebase commits that other people already depend on. Resolve conflicts, test, then continue with `git rebase --continue` or abort with `git rebase --abort`.