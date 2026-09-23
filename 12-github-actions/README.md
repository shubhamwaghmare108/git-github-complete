# 12 — GitHub Actions

Actions automate CI/CD and repository workflows.

Typical pipeline:
`push/PR → checkout → setup runtime → install dependencies → lint → test → build → publish/deploy`

Workflow files live under `.github/workflows/`.

Key concepts: events, jobs, steps, runners, actions, matrices, artifacts, environments, permissions and secrets.