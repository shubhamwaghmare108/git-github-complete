# Labs 071-080 — Advanced Workflows

## Lab 071 — Release with a tag
**Objective:** Mark a production-ready commit. **Commands:** `git tag -a v1.0.0 -m "Release 1.0.0"`; `git push origin v1.0.0`. **Expected:** Tag is visible remotely. **Task:** Inspect tag commit. **Challenge:** Push tags deliberately rather than accidentally. **Solution:** Push the intended tag explicitly. **Interview:** Why tag releases?

## Lab 072 — Create a release checklist
**Objective:** Make releases repeatable. **Task:** Define version, tests, changelog, tag, release notes, rollback, and verification. **Expected:** Checklist can be reused. **Challenge:** Add owner and evidence fields. **Solution:** Require objective verification before publishing. **Interview:** What is a release artifact?

## Lab 073 — Build a GitHub Pages site
**Objective:** Publish static documentation. **Task:** Create a simple HTML or Markdown site and configure GitHub Pages in a practice repository. **Expected:** Site is published according to repository settings. **Challenge:** Add navigation. **Solution:** Keep site files deterministic and documented. **Interview:** What is GitHub Pages used for?

## Lab 074 — Document a deployment
**Objective:** Turn deployment into a reproducible process. **Task:** Write prerequisites, commands, environment variables, verification, rollback, and troubleshooting. **Expected:** Another learner can follow the document. **Challenge:** Add a smoke test. **Solution:** Treat deployment docs as code. **Interview:** Why document rollback?

## Lab 075 — Create a hotfix
**Objective:** Practice urgent production repair. **Workflow:** Start from release/main, create hotfix branch, make minimal fix, test, PR, merge, tag if appropriate. **Expected:** Small traceable change. **Challenge:** Backport to a maintenance branch. **Solution:** Cherry-pick the verified fix where appropriate. **Interview:** Why keep hotfixes small?

## Lab 076 — Backport a commit
**Objective:** Move a targeted fix to an older maintenance branch. **Commands:** Switch maintenance branch; `git cherry-pick <fix-commit>`. **Expected:** Fix appears with a new commit ID. **Task:** Run tests. **Challenge:** Resolve conflicts. **Solution:** Treat conflict resolution as a code review point. **Interview:** What is backporting?

## Lab 077 — Create a reusable team workflow
**Objective:** Standardize local contribution steps. **Task:** Write a team workflow covering branch naming, commits, PRs, reviews, CI, and merge. **Expected:** New contributors can follow it. **Challenge:** Add exceptions for hotfixes. **Solution:** Document normal path and explicit exceptions. **Interview:** What makes a workflow scalable?

## Lab 078 — Diagnose a failing CI run
**Objective:** Debug automation methodically. **Task:** Identify trigger, runner, checkout, dependency installation, failing command, logs, and artifact output. **Expected:** Root cause is separated from symptoms. **Challenge:** Reproduce failure locally. **Solution:** Start at the first meaningful error, then verify assumptions. **Interview:** Why is the first error often more useful than the final error?

## Lab 079 — Create a rollback plan
**Objective:** Prepare for failed releases. **Task:** Define rollback for application code, database changes, configuration, and release tags. **Expected:** Plan includes trigger, owner, commands, verification, and communication. **Challenge:** Add a forward-fix alternative. **Solution:** Prefer reversible, tested procedures. **Interview:** What makes rollback safe?

## Lab 080 — Run a team simulation
**Objective:** Combine branches, PRs, review, CI, release, and hotfix skills. **Scenario:** Three contributors work on one repository. **Expected:** No direct unreviewed changes to main and all changes are traceable. **Task:** Produce a timeline. **Challenge:** Introduce a conflict and failed CI check. **Solution:** Resolve each through the documented workflow. **Interview:** Which controls reduce integration risk?