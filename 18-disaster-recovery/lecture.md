# Disaster Recovery — Full Lecture

### Incident 1: deleted branch
```bash
git reflog
git branch recovery <sha>
```

### Incident 2: wrong reset
Find the previous HEAD in reflog and create a recovery branch before changing anything else.

### Incident 3: bad merge
Inspect the merge commit, determine whether a revert or a corrected follow-up is appropriate, and preserve shared history when possible.

### Incident 4: leaked secret
Rotate/revoke first. Then investigate usage and clean repository history if required.

### Golden rule
**Stop, inspect, preserve evidence, recover, then clean up.**