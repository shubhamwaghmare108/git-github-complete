# 16 — GitHub REST API

The GitHub API lets scripts and applications automate repository operations.

Example with GitHub CLI:
```bash
gh api user
gh api repos/OWNER/REPO
```

For production automation, authenticate securely, request only required permissions, handle pagination/rate limits, and never hard-code tokens.