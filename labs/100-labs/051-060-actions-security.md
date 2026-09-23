# Labs 051-060 — Actions and Security

## Lab 051 — Read a workflow
**Objective:** Understand workflow YAML. **Task:** Inspect `12-github-actions/basic-ci.yml`. **Expected:** You can identify name, trigger, jobs, runner, and steps. **Challenge:** Rewrite it in your own words. **Solution:** Map event → workflow → job → step. **Interview:** What is a GitHub Actions workflow?

## Lab 052 — Create a minimal CI workflow
**Objective:** Automate a repository check. **Commands:** Create `.github/workflows/ci.yml` with checkout and a shell test. **Expected:** Workflow runs on push/PR. **Task:** Inspect the Actions run. **Challenge:** Add a second validation step. **Solution:** Keep steps small and observable. **Interview:** What triggers a workflow?

## Lab 053 — Restrict GITHUB_TOKEN permissions
**Objective:** Apply least privilege. **Task:** Add `permissions: contents: read` to a documentation workflow. **Expected:** Workflow receives only required repository access. **Challenge:** Determine which permissions a write operation needs. **Solution:** Grant only the documented minimum. **Interview:** Why restrict token permissions?

## Lab 054 — Use a secret
**Objective:** Avoid hard-coded credentials. **Task:** Create a dummy repository secret and reference it as an environment variable in a test workflow. **Expected:** Secret is not committed to source. **Challenge:** Explain why echoing secrets is unsafe. **Solution:** Never print credential values. **Interview:** Where should CI secrets live?

## Lab 055 — Detect a leaked secret
**Objective:** Practice incident response. **Scenario:** A token was accidentally committed. **Task:** Revoke/rotate it first, then remove it from current files and assess history. **Expected:** Credential is invalidated and repository no longer exposes it in current state. **Challenge:** Explain why deleting the line alone may not erase history. **Solution:** Treat the credential as compromised and rotate it. **Interview:** What is the first action after a credential leak?

## Lab 056 — Add a dependency review mindset
**Objective:** Review third-party actions and packages. **Task:** Inspect workflow actions and dependency versions. **Expected:** Every dependency has an identified source/version. **Challenge:** Prefer immutable references for high-security workflows. **Solution:** Evaluate provenance, permissions, and update process. **Interview:** Why can third-party Actions be a supply-chain risk?

## Lab 057 — Protect the main branch
**Objective:** Design merge controls. **Task:** On a practice repository, require PR review and passing checks before merge. **Expected:** Direct unsafe changes are discouraged/blocked by configured rules. **Challenge:** Add required status checks. **Solution:** Configure repository rules/rulesets appropriate to the team. **Interview:** What is branch protection?

## Lab 058 — Secure pull-request workflows
**Objective:** Identify risky workflow triggers. **Scenario:** An untrusted PR can influence workflow-controlled code. **Task:** Inspect use of privileged tokens and `pull_request_target`. **Expected:** You can explain why untrusted input must not gain write-capable secrets. **Challenge:** Redesign a risky workflow using least privilege. **Solution:** Keep untrusted code isolated from privileged credentials. **Interview:** Why is `pull_request_target` sensitive?

## Lab 059 — Add a status check
**Objective:** Make quality visible before merge. **Task:** Create a CI job that fails when README.md is missing. **Expected:** Broken state blocks the check. **Challenge:** Add multiple independent checks. **Solution:** Use separate steps/jobs with clear names. **Interview:** What is a required status check?

## Lab 060 — Audit repository security
**Objective:** Perform a basic security review. **Checklist:** secrets, workflow permissions, branch rules, dependencies, issue settings, collaborators, and `.gitignore`. **Expected:** Findings are documented with severity and remediation. **Challenge:** Create a remediation issue for each finding. **Solution:** Fix exposure first, then improve preventive controls. **Interview:** What is least privilege?