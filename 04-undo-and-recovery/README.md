# 04 — Undo and Recovery

| Command | Typical purpose |
|---|---|
| `git restore` | restore file contents / unstage |
| `git reset` | move local history pointer |
| `git revert` | create a new commit that reverses a commit |
| `git reflog` | recover reachable previous local references |

## Reset modes
```bash
git reset --soft HEAD~1
git reset --mixed HEAD~1
git reset --hard HEAD~1
```

Treat `--hard`, force-push, and destructive cleanup as high-risk operations. Verify with `git status` and `git log` first.