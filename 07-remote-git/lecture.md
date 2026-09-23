# Remote Git — Full Lecture

```bash
git remote -v
git remote add origin <url>
git fetch origin
git branch -r
git switch -c feature/x
git push -u origin feature/x
git pull --rebase origin main
```

`fetch` downloads remote information without integrating it into the current branch. `pull` is fetch plus integration. Prefer understanding the fetched state before resolving divergence.

### Exercise
Create a local branch, push it, fetch from another clone, inspect `origin/<branch>`, and integrate changes.