# GitHub Actions — Full Lecture

Actions workflows are YAML automation definitions stored under `.github/workflows/`.

Core concepts:
`event → workflow → jobs → steps → runner`

Typical CI:
`checkout → setup runtime → install → lint → test → build`

Set explicit `permissions` so `GITHUB_TOKEN` has only the access needed by the workflow. GitHub supports permissions such as `contents`, `issues`, `pull-requests`, `actions`, `security-events` and others. citeturn0search11

### Lab
Create a workflow for push and pull request events. Make one test fail, inspect logs, fix it, and verify a successful run.