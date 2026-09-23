# Labs 091-100 — Capstone Engineering

## Lab 091 — Design a repository from scratch
**Objective:** Apply repository architecture skills. **Task:** Define README, license, contributing, security, ignore rules, source/docs/tests, and workflows. **Expected:** A coherent repository skeleton. **Challenge:** Explain every top-level directory. **Solution:** Keep structure purpose-driven. **Interview:** What belongs in a good repository README?

## Lab 092 — Build a documentation CI pipeline
**Objective:** Validate documentation automatically. **Task:** Create a workflow that checks required Markdown files and exits non-zero when one is missing. **Expected:** Push and PR checks run. **Challenge:** Add a link or heading check. **Solution:** Keep CI deterministic and read-only where possible. **Interview:** What makes CI trustworthy?

## Lab 093 — Team branching simulation
**Objective:** Simulate four contributors. **Task:** Each contributor creates a branch, commits, opens a PR, responds to review, and merges. **Expected:** Main history is reviewable. **Challenge:** Two branches modify the same line. **Solution:** Resolve conflict in one branch and re-run checks. **Interview:** How should teams handle conflicting changes?

## Lab 094 — Release automation design
**Objective:** Design a release workflow. **Task:** Trigger on a version tag, run tests, create release notes/artifacts, and record verification. **Expected:** Design identifies permissions and failure points. **Challenge:** Add rollback. **Solution:** Separate build, verification, publication, and rollback responsibilities. **Interview:** Why separate build and release stages?

## Lab 095 — Repository security audit
**Objective:** Perform an end-to-end audit. **Task:** Inspect secrets, Actions permissions, third-party actions, branch rules, collaborators, dependencies, and ignore files. **Expected:** Findings and remediation plan. **Challenge:** Prioritize by exposure and impact without using vague severity labels. **Solution:** Describe concrete attack surface and mitigation. **Interview:** What is a supply-chain attack?

## Lab 096 — API-based repository dashboard
**Objective:** Build a small CLI dashboard. **Task:** Collect repository metadata, open issues, PR counts, and workflow status through GitHub CLI/API. **Expected:** Repeatable report. **Challenge:** Handle pagination and API errors. **Solution:** Use structured output and explicit error handling. **Interview:** Why prefer APIs for automation?

## Lab 097 — Monorepo change workflow
**Objective:** Handle a repository containing multiple components. **Task:** Define path ownership, tests, PR rules, and release strategy. **Expected:** Changes can be isolated by component. **Challenge:** Add component-specific CI. **Solution:** Use path-aware workflows and ownership rules where appropriate. **Interview:** What is a monorepo?

## Lab 098 — Open-source contribution simulation
**Objective:** Practice contributing without direct write access. **Workflow:** Fork → clone → branch → change → test → push → PR → review. **Expected:** Contribution is isolated from upstream main. **Challenge:** Sync fork after upstream changes. **Solution:** Add upstream remote and fetch/rebase or merge deliberately. **Interview:** Why use forks?

## Lab 099 — Full incident simulation
**Objective:** Recover from multiple failures. **Scenario:** A bad commit reaches main, CI fails, and a credential appears in history. **Task:** Contain credential, preserve evidence, restore stable code, repair forward, and document actions. **Expected:** Safe recovery sequence. **Challenge:** Coordinate two responders. **Solution:** Separate security containment from Git history repair. **Interview:** What should happen first in a credential incident?

## Lab 100 — Final Git/GitHub practical exam
**Objective:** Demonstrate complete workflow competence. **Scenario:** Start with a local project and empty GitHub repository. **Task:** Initialize, commit, branch, push, open issue, create PR, pass CI, resolve review comments, merge, tag a release, and produce a recovery note. **Expected:** Fully traceable repository lifecycle. **Challenge:** Introduce one controlled conflict and one failed CI check. **Solution:** Diagnose, fix, verify, and document each event. **Interview:** Explain the complete path from working-tree edit to released software.