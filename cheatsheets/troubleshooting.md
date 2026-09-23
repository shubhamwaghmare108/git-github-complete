# Troubleshooting Cheat Sheet

### Wrong branch
```bash
git status
git branch --show-current
```

### Lost local commit
```bash
git reflog
git branch recovery <sha>
```

### Push rejected
```bash
git fetch origin
git log --oneline --graph --all
git pull --rebase
```

### Merge conflict
```bash
git status
# edit conflict markers
git add <resolved-file>
git commit
```

### Detached HEAD
```bash
git switch -c recovery-branch
```