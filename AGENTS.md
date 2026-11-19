# Rules for any coding agent working in this repository

Instruction hierarchy: the current GitHub issue wins over this file only for scope; this file wins for process and honesty.

1. Do exactly what the issue asks. Do not add features, refactor unrelated code or rename things that were not requested.
2. If a requirement is ambiguous or two requirements conflict, stop and ask in the issue before coding. Do not guess.
3. Work only on the branch for this issue and open one pull request. Never push to main.
4. Write tests first or with the code. A task is done only when tests pass in CI. Paste the CI result in the pull request.
5. Never mark anything complete, production-ready or working unless a test you ran proves it. Say "not built" or "requires configuration" instead.
6. Never fake data, statuses, files, metrics or buttons. Unbuilt features are disabled with a visible reason.
7. Never print, log or commit secrets. Read credentials from environment variables only.
8. Every quality check returns PASS, FAIL, WARNING or NOT_RUN. Never return PASS for a check that did not run.
9. Original uploaded files are immutable. Every operation creates a new versioned asset.
10. Never silently resample. Never claim a DPI unless pixel size and embedded metadata both match.
11. Follow the pitfall list in docs/pitfalls.md; each item has a regression test.
12. Keep pull requests small enough to review. Report what changed, what was tested, what is missing and what you need from me.

## Required pull request report
1. Done and tested (item, test name, result)
2. Done but not tested (and why)
3. Not built
4. Requires configuration (exact credential, model or licence)
5. Benchmark numbers vs targets
6. Known defects and risks
7. What I need from you next
