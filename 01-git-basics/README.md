# 01 — Git Basics

## Mental model
`Working Directory → Staging Area → Local Repository → Remote Repository`

## Core commands
```bash
git init
git clone <url>
git status
git add <file>
git add .
git commit -m "message"
git log --oneline --graph --decorate --all
git diff
git diff --staged
git show <commit>
```

## Practice
Create a repository, make three commits, inspect each snapshot, and compare staged versus unstaged changes.