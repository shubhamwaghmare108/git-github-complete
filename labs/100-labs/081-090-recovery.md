# Labs 081-090 — Disaster Recovery and Troubleshooting

## Lab 081 — Recover a deleted local branch
**Objective:** Recover a branch reference. **Commands:** `git reflog`; `git switch -c recovery <lost-commit>`. **Expected:** Work is reachable again. **Task:** Verify commits. **Challenge:** Recover after several HEAD moves. **Solution:** Identify the correct reflog entry. **Interview:** What information does reflog preserve?

## Lab 082 — Recover from reset --hard
**Objective:** Practice recovery from an accidental reset. **Scenario:** A branch was reset before pushing. **Task:** Use reflog to locate the previous tip and create a recovery branch. **Expected:** Lost commits are reachable. **Challenge:** Restore the original branch carefully. **Solution:** Verify first, then move the ref. **Interview:** Why should you inspect before repairing?

## Lab 083 — Abort a merge
**Objective:** Exit a problematic merge safely. **Commands:** Start a conflicting merge; `git merge --abort`. **Expected:** Pre-merge state returns. **Task:** Confirm status and diff. **Challenge:** Explain when abort may not be available/appropriate. **Solution:** Inspect state before using recovery commands. **Interview:** What does merge --abort attempt to restore?

## Lab 084 — Abort a rebase
**Objective:** Exit a failed rebase. **Commands:** During conflict, `git rebase --abort`. **Expected:** Branch returns to pre-rebase state. **Task:** Inspect reflog. **Challenge:** Continue instead of aborting. **Solution:** Fix, stage, continue when resolution is correct. **Interview:** Difference between continue and abort?

## Lab 085 — Recover an unpushed commit
**Objective:** Recover a commit after changing branches. **Task:** Search `git reflog` and inspect candidate commits. **Expected:** Commit can be reached by a new branch. **Challenge:** Find it using `git fsck` only in a controlled practice repository. **Solution:** Prefer reflog first. **Interview:** What is dangling Git data?

## Lab 086 — Diagnose detached HEAD
**Objective:** Convert detached work into a branch. **Commands:** `git status`; `git switch -c rescue-work`. **Expected:** Detached commit becomes part of a named branch. **Task:** Merge or PR the branch later. **Challenge:** Explain how detached HEAD happens. **Solution:** Checkout of a commit/tag without switching to a branch detaches HEAD. **Interview:** Is detached HEAD itself an error?

## Lab 087 — Repair a bad merge
**Objective:** Correct a merge that introduced wrong content. **Scenario:** Bad merge is already published. **Task:** Decide whether to revert the merge or repair forward based on history. **Expected:** Shared history remains stable. **Challenge:** Compare with rewriting history on a private branch. **Solution:** Published shared history often favors a new corrective commit. **Interview:** Why is revert safer than reset on shared history?

## Lab 088 — Recover after an accidental force push
**Objective:** Investigate overwritten remote history. **Task:** Use local clones, reflogs, tags, or known commit IDs to locate lost commits; coordinate before restoring. **Expected:** Recovery path is documented. **Challenge:** Recreate the remote branch only after verifying the desired tip. **Solution:** Preserve evidence and use force-with-lease where rewriting is unavoidable. **Interview:** Why coordinate recovery?

## Lab 089 — Secret leak response drill
**Objective:** Practice credential incident response. **Scenario:** API key committed to a public branch. **Task:** Revoke/rotate key, identify exposure, remove from active files, assess history and logs, and document remediation. **Expected:** Credential cannot be used. **Challenge:** Add preventive controls. **Solution:** Rotation is more important than merely deleting text. **Interview:** Why is history cleanup not a substitute for revocation?

## Lab 090 — Create a recovery runbook
**Objective:** Convert lessons into operational documentation. **Task:** Write steps for deleted branch, bad reset, merge conflict, accidental force push, and leaked secret. **Expected:** Runbook includes detection, containment, recovery, verification, and prevention. **Challenge:** Add decision points. **Solution:** Make commands copyable but require inspection before destructive actions. **Interview:** Why separate containment from recovery?