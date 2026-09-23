# GitHub API — Full Lecture

The API enables automation beyond standard Git commands. Start with read-only requests and add write operations only when required.

Using GitHub CLI:
```bash
gh api user
gh api repos/OWNER/REPO
gh api repos/OWNER/REPO/issues
```

Production automation should handle authentication, permissions, pagination, rate limits and errors. Never hard-code access tokens.