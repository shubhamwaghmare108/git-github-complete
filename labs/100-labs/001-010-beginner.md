# Labs 001-010 — Git Foundations

## Lab 001 — Install and verify Git
**Objective:** Verify a working Git installation.  
**Scenario:** A new developer is preparing a machine.  
**Commands:** `git --version`, `git config --global user.name "Student"`, `git config --global user.email "student@example.com"`.  
**Expected:** Git version and configured identity are displayed.  
**Task:** Run the commands and inspect `git config --global --list`.  
**Challenge:** Explain local vs global configuration.  
**Solution:** Git must be installed; set identity with the two config commands.  
**Interview:** Why does Git need user.name and user.email?

## Lab 002 — Create a repository
**Objective:** Initialize a repository.  
**Commands:** `mkdir git-lab-002 && cd git-lab-002 && git init`.  
**Expected:** A `.git` directory is created.  
**Task:** Run `git status`.  
**Challenge:** Locate `.git` with your OS file tools.  
**Solution:** `git init` creates the repository metadata.  
**Interview:** What does `git init` create?

## Lab 003 — Track the first file
**Objective:** Understand untracked → staged.  
**Commands:** `echo "# Lab 003" > README.md`, `git status`, `git add README.md`, `git status`.  
**Expected:** README changes from untracked to staged.  
**Task:** Explain the two status outputs.  
**Challenge:** Stage only one of two files.  
**Solution:** Use `git add <file>` instead of `git add .`.  
**Interview:** Why is staging separate from committing?

## Lab 004 — Make the first commit
**Objective:** Create a local snapshot.  
**Commands:** `git commit -m "Add README"`, `git log --oneline`.  
**Expected:** One commit appears.  
**Task:** Inspect the commit with `git show`.  
**Challenge:** Write a meaningful commit message.  
**Solution:** Commit staged changes with an imperative, specific message.  
**Interview:** Is a commit the same as a file backup?

## Lab 005 — Modify and inspect
**Objective:** Observe tracked-file changes.  
**Commands:** Edit README, then `git status`, `git diff`.  
**Expected:** Git shows unstaged modifications.  
**Task:** Read the diff before staging.  
**Challenge:** Make two edits and stage only one.  
**Solution:** Use `git add -p` for selective staging.  
**Interview:** What does `git diff` show by default?

## Lab 006 — Selective staging
**Objective:** Stage part of a working tree safely.  
**Commands:** `git add -p README.md`, then `git diff --cached`.  
**Expected:** Only selected hunks are staged.  
**Task:** Commit the staged hunk.  
**Challenge:** Leave an unrelated edit unstaged.  
**Solution:** Use interactive staging and verify with cached diff.  
**Interview:** Why inspect `git diff --cached`?

## Lab 007 — Write a useful .gitignore
**Objective:** Ignore generated/local files.  
**Scenario:** Python project creates `__pycache__`, `.venv`, and `.env`.  
**Commands:** Create `.gitignore` containing those patterns; run `git status`.  
**Expected:** Ignored files do not appear as untracked.  
**Task:** Add a rule for `.DS_Store`.  
**Challenge:** Explain why secrets belong in `.gitignore`.  
**Solution:** Add environment-specific/generated patterns before staging.  
**Interview:** Does .gitignore untrack an already committed file?

## Lab 008 — Amend the latest commit
**Objective:** Correct the latest local commit.  
**Commands:** Make a small edit, `git add README.md`, `git commit --amend -m "Improve README"`.  
**Expected:** The latest commit is replaced.  
**Task:** Inspect the new hash.  
**Challenge:** Explain why amend is risky after sharing.  
**Solution:** Amend is appropriate for an unpublished latest commit.  
**Interview:** What happens to the old commit hash?

## Lab 009 — Inspect commit history
**Objective:** Read history effectively.  
**Commands:** `git log --oneline --decorate --graph --all`, `git show HEAD`.  
**Expected:** History and current ref are visible.  
**Task:** Identify parent and changed files.  
**Challenge:** Find a commit by message.  
**Solution:** Use `git log --grep="keyword"`.  
**Interview:** What is HEAD?

## Lab 010 — Create a branch
**Objective:** Isolate work.  
**Commands:** `git switch -c feature/readme`, edit README, commit, `git switch main`.  
**Expected:** Main remains unchanged while feature has its commit.  
**Task:** Compare `git log --graph --all`.  
**Challenge:** Create another feature branch.  
**Solution:** Use `git switch -c <branch>`.  
**Interview:** What does a branch point to?