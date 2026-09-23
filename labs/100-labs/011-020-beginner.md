# Labs 011-020 — Core Workflow

## Lab 011 — Restore unstaged changes
**Objective:** Discard a safe local edit. **Commands:** Edit a tracked file; `git restore file.txt`; `git status`. **Expected:** Working-tree edit disappears. **Task:** Verify with `git diff`. **Challenge:** Explain why this cannot recover an uncommitted edit. **Solution:** Restore replaces the working copy from the index/HEAD depending on state. **Interview:** What does `git restore` replace?

## Lab 012 — Unstage a file
**Objective:** Move a file out of staging. **Commands:** `git add file.txt`; `git restore --staged file.txt`. **Expected:** File becomes modified, not staged. **Task:** Check status. **Challenge:** Keep the working edit. **Solution:** `restore --staged` changes only the index. **Interview:** How is unstage different from discard?

## Lab 013 — Use git diff modes
**Objective:** Compare working tree, index, and HEAD. **Commands:** `git diff`, `git diff --cached`, `git diff HEAD`. **Expected:** Three views show different boundaries. **Task:** Describe each. **Challenge:** Stage only one hunk. **Solution:** Use `git add -p`. **Interview:** Which command compares staged changes with HEAD?

## Lab 014 — Rename a file
**Objective:** Record a rename cleanly. **Commands:** `git mv old.txt new.txt`; `git status`; commit. **Expected:** Rename is detected. **Task:** Inspect `git show --stat`. **Challenge:** Rename and edit in one commit. **Solution:** `git mv` stages the rename. **Interview:** Does Git store a rename object?

## Lab 015 — Delete a tracked file
**Objective:** Remove a tracked file. **Commands:** `git rm old.txt`; commit. **Expected:** File deletion is staged. **Task:** Inspect history. **Challenge:** Delete from disk first and stage with `git add -u`. **Solution:** Both approaches update the index. **Interview:** What does `git rm` do?

## Lab 016 — Read .gitignore behavior
**Objective:** Diagnose an ignored path. **Commands:** `git check-ignore -v path/to/file`. **Expected:** Matching rule and source are shown. **Task:** Add a project-specific rule. **Challenge:** Explain global excludes. **Solution:** Use `git check-ignore` for diagnosis. **Interview:** Where can ignore rules come from?

## Lab 017 — Use git stash
**Objective:** Temporarily shelve work. **Commands:** Edit file; `git stash push -m "WIP"`; `git stash list`; `git stash pop`. **Expected:** Work disappears then returns. **Task:** Inspect stash with `git stash show -p`. **Challenge:** Keep multiple stashes. **Solution:** Name stashes and apply the intended one. **Interview:** Is stash a permanent backup?

## Lab 018 — Stash including untracked files
**Objective:** Save new files temporarily. **Commands:** Create file; `git stash push -u -m "include new file"`. **Expected:** Untracked file enters stash. **Task:** Apply it later. **Challenge:** Compare `-u` and `-a`. **Solution:** `-u` includes untracked; `-a` also includes ignored files. **Interview:** When should stash be avoided?

## Lab 019 — Tag a release
**Objective:** Mark a stable commit. **Commands:** `git tag -a v1.0.0 -m "First release"`; `git show v1.0.0`. **Expected:** Annotated tag metadata appears. **Task:** List tags. **Challenge:** Create a lightweight tag and compare. **Solution:** Use `git tag v1.0.1` for lightweight tags. **Interview:** What is a tag used for?

## Lab 020 — Find lost work with reflog
**Objective:** Recover a moved branch/HEAD. **Commands:** `git reflog`; identify a prior commit; `git show <hash>`. **Expected:** Previous HEAD positions are visible. **Task:** Create a recovery branch. **Challenge:** Recover after a reset. **Solution:** `git switch -c recovery <hash>`. **Interview:** Why is reflog local?