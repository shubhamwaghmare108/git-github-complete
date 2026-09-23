# Git Cheat Sheet

```bash
git init
git clone <url>
git status
git add .
git commit -m "message"
git log --oneline --graph --all
git diff
git restore <file>
git restore --staged <file>
git reset --soft HEAD~1
git reset --mixed HEAD~1
git reset --hard HEAD~1
git revert <commit>
git reflog
git switch -c feature/x
git merge feature/x
git rebase main
git cherry-pick <commit>
git stash
git fetch origin
git pull --rebase
git push -u origin feature/x
git tag v1.0.0
```