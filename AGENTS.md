# Rules for any coding agent working in this repository

Instruction hierarchy: the current GitHub issue wins over this file only for scope; this file wins for process and honesty.

1. Do exactly what the issue asks. Do not add features, refactor unrelated code or rename things that were not requested.
2. If a requirement is ambiguous or conflicts with another requirement, stop and ask in the issue before coding.
3. Work only on the branch for this issue and open one pull request. Never push to main.
4. Write tests first or with the code. A task is done only when tests pass in CI.
5. Never mark anything complete or production-ready unless a test you ran proves it.
6. Never fake data, statuses, files, metrics or buttons.
7. Never print, log or commit secrets. Read credentials from environment variables only.
8. Every quality check returns PASS, FAIL, WARNING or NOT_RUN.
9. Original uploaded files are immutable. Every operation creates a new versioned asset.
10. Never silently resample. Never claim DPI unless pixel size and embedded metadata both match.
11. Follow `docs/pitfalls.md`; each pitfall requires a regression test.
12. Keep pull requests small enough to review and report tests, missing work and risks.
