# 18 — Disaster Recovery

## Common incidents
- accidental commit
- accidental reset
- deleted branch
- detached HEAD
- bad merge
- lost local commit
- wrong remote
- leaked secret

First steps:
```bash
git status
git reflog
git log --all --decorate --oneline
git fsck --lost-found
```

Do not run destructive cleanup until the desired commits are safely identified.