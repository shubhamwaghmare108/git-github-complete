# Branching — Full Lecture

A branch is a movable reference to a commit. Creating a branch is cheap because Git stores a reference rather than copying the project.

```bash
git branch
git switch -c feature/login
git switch main
git branch -m feature/login feature/auth
git branch -d feature/auth
```

### Branch strategy
Keep branches focused and short-lived. Keep `main` releasable when practical.

### Exercise
Create `feature/a` and `feature/b`, make two independent commits, inspect the graph, then merge both.