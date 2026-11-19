# One-time GitHub setup (done by the repository owner)

1. Merge the pull request that adds these rule files.
2. Settings > Branches > add a rule for main: require a pull request, require status checks (after the first CI run exists), block direct pushes.
3. Settings > Actions > General: allow actions. Settings > Code security: enable Dependabot alerts and updates.
4. Create labels and milestones M0 to M8 (Issues > Labels, Issues > Milestones).
5. Open an issue from docs/issues/M0.md using the Milestone template.
6. Assign the issue to your coding agent and paste the master prompt as its first instruction.
7. Add repository secrets only when a milestone needs them, by name, in Settings > Secrets and variables > Actions.

Optional, if you use the GitHub CLI (gh):

    for i in 0 1 2 3 4 5 6 7 8; do gh label create "M$i" --color 1d76db; gh api repos/:owner/:repo/milestones -f title="M$i"; done
