# Labs 021-030 — History and Branching

## Lab 021 — Compare branches
**Objective:** Compare branch tips. **Commands:** `git log main..feature --oneline`; `git diff main...feature`. **Expected:** Unique commits and cumulative changes are visible. **Task:** Explain two-dot vs three-dot. **Challenge:** Find commits unique to main. **Solution:** Reverse the range. **Interview:** What does `A..B` mean?

## Lab 022 — Merge a feature
**Objective:** Integrate a branch. **Commands:** Create feature commit; switch main; `git merge feature`. **Expected:** Feature becomes reachable from main. **Task:** Inspect graph. **Challenge:** Force a merge commit with `--no-ff`. **Solution:** Use the appropriate merge strategy. **Interview:** What is a fast-forward merge?

## Lab 023 — Resolve a merge conflict
**Objective:** Practice conflict resolution. **Scenario:** Both branches edit the same lines. **Commands:** `git merge feature`; edit conflict markers; `git add file`; `git commit`. **Expected:** Merge completes. **Task:** Explain which content was retained. **Challenge:** Abort and retry. **Solution:** `git merge --abort`. **Interview:** Where do conflict markers come from?

## Lab 024 — Rebase a feature
**Objective:** Replay feature commits onto updated main. **Commands:** `git switch feature`; `git rebase main`. **Expected:** Feature commits receive new IDs. **Task:** Inspect graph. **Challenge:** Resolve a rebase conflict. **Solution:** Fix file, `git add`, `git rebase --continue`; abort with `git rebase --abort`. **Interview:** Why does rebase rewrite history?

## Lab 025 — Cherry-pick a fix
**Objective:** Copy one commit onto another branch. **Commands:** `git cherry-pick <commit>`. **Expected:** A new commit applies the selected change. **Task:** Inspect the new hash. **Challenge:** Resolve a cherry-pick conflict. **Solution:** Fix, add, `git cherry-pick --continue`; abort when necessary. **Interview:** Why is the resulting commit hash different?

## Lab 026 — Use git bisect
**Objective:** Locate a regression. **Commands:** `git bisect start`; `git bisect bad`; `git bisect good <known-good>`; test each checkout; mark good/bad; `git bisect reset`. **Expected:** Git identifies a likely first bad commit. **Task:** Record the culprit. **Challenge:** Automate with `git bisect run`. **Solution:** Provide a test command with a reliable exit code. **Interview:** What algorithm does bisect exploit?

## Lab 027 — Inspect a commit precisely
**Objective:** Extract targeted history. **Commands:** `git show --stat <commit>`; `git show <commit> -- path`; `git log -S"keyword" --oneline`. **Expected:** Relevant historical changes are isolated. **Task:** Find when a string changed. **Challenge:** Use `-G"regex"`. **Solution:** Pick -S for string-count changes and -G for regex matching. **Interview:** What is pickaxe search?

## Lab 028 — Use blame responsibly
**Objective:** Trace line history. **Commands:** `git blame -L 10,20 file`; `git show <commit>`. **Expected:** Commit/author metadata appears. **Task:** Follow the commit context. **Challenge:** Identify whether blame points to original author or last modifier. **Solution:** Blame reports the commit that last changed each line. **Interview:** Why should blame not be used to assign blame socially?

## Lab 029 — Create and inspect detached HEAD
**Objective:** Understand detached HEAD. **Commands:** `git switch --detach <tag>`; `git status`; create a commit; `git switch main`. **Expected:** HEAD is detached. **Task:** Recover the detached commit using reflog. **Challenge:** Create a branch before leaving. **Solution:** `git switch -c experiment`. **Interview:** What does detached HEAD mean?

## Lab 030 — Compare merge and rebase
**Objective:** Select an integration technique based on history requirements. **Scenario:** Team branch is private; main is shared. **Commands:** Draw both graphs, perform each on separate test branches. **Expected:** Graph differences are clear. **Task:** Document trade-offs. **Challenge:** Explain why rewriting shared history is risky. **Solution:** Rebase rewrites commit ancestry; shared commits should generally not be rewritten casually. **Interview:** When would you prefer merge?