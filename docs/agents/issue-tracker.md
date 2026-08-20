# Issue tracker: GitHub

Issues and specifications for this repository live in GitHub Issues. Use the `gh` CLI for issue operations.

## Conventions

- Create an issue with `gh issue create --title "..." --body "..."`.
- Read an issue with `gh issue view <number> --comments`.
- List issues with `gh issue list`, adding label and state filters as needed.
- Comment with `gh issue comment <number> --body "..."`.
- Add or remove labels with `gh issue edit <number> --add-label "..."` or `--remove-label "..."`.
- Close an issue with `gh issue close <number> --comment "..."`.

Run commands inside this repository so `gh` can infer `dumptruckman/bot-tournament-runner` from the Git remote.

## Pull requests in triage

External pull requests are not a request source. The `triage` skill processes issues only. Review pull requests through the repository's normal code-review workflow.

## Skill operations

When a skill says "publish to the issue tracker," create a GitHub issue.

When a skill says "fetch the relevant ticket," run:

```sh
gh issue view <number> --comments
```

## Wayfinding operations

The `wayfinder` skill represents a work map as one GitHub issue with child issues.

- Label the map `wayfinder:map`.
- Link child tickets with GitHub sub-issues when available.
- If sub-issues are unavailable, add children to a task list in the map and put `Part of #<map>` at the top of each child.
- Label child tickets `wayfinder:research`, `wayfinder:prototype`, `wayfinder:grilling`, or `wayfinder:task`.
- Use GitHub issue dependencies for blocking relationships when available.
- If dependencies are unavailable, put `Blocked by: #<number>` at the top of the child issue.
- Claim work with `gh issue edit <number> --add-assignee @me`.
- Resolve work by commenting with the result, closing the child issue, and adding the result link to the map.
