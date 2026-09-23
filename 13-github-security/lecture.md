# GitHub Security — Full Lecture

Never commit credentials. Use repository/environment secrets or short-lived authentication mechanisms where appropriate.

Security topics:
- least-privilege workflow permissions
- secret rotation
- dependency security
- code scanning
- branch/ruleset protection
- trusted versus untrusted workflow contexts

GitHub documents elevated risks when privileged workflows check out untrusted pull-request code, particularly with `pull_request_target`. citeturn0search4turn0search7

### Lab
Review a workflow and identify unnecessary permissions, unsafe triggers, exposed secrets and unpinned third-party actions.