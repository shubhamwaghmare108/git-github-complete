# Undo and Recovery — Full Lecture

Choose the operation by the situation.

| Situation | Command |
|---|---|
| discard working-file edits | `git restore file` |
| unstage a file | `git restore --staged file` |
| undo a published commit | `git revert <sha>` |
| move local branch backward | `git reset` |
| locate previous local references | `git reflog` |

### Recovery lab
Make a commit, reset it away, then recover it:
```bash
git reset --hard HEAD~1
git reflog
git branch recovery <lost-sha>
```

Never use `reset --hard` as a casual undo command when uncommitted work matters.