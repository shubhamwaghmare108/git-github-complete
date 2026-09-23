# Git Basics — Full Lecture

## 1. What is Git?
Git is a distributed version control system. It records project history as commits and lets developers work safely in parallel.

## 2. The four areas
`Working Directory → Staging Area → Local Repository → Remote Repository`

- Working directory: files you are editing.
- Staging area/index: exact content selected for the next commit.
- Local repository: committed history in `.git`.
- Remote: another Git repository, commonly hosted on GitHub.

## 3. First workflow
```bash
git init
git status
git add README.md
git diff --staged
git commit -m "docs: add README"
git log --oneline
```

## 4. Why staging matters
Staging lets one commit contain only a logical part of the current work.

## 5. Exercise
Create five commits. Before every commit, inspect `git status`, `git diff`, and `git diff --staged`.