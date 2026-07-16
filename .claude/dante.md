# Dante workflow: kcd-scripts

Universal guidance for Dante workers operating in this repository.
Instructions in the epic supersede anything here.

## Development

- Work only inside your task's worktree, and only on files you have
  reserved in the shared filelock.
- Match the surrounding code's style and conventions.

## Validation

When a change is ready, run the repository's checks from the worktree
root:

- `npm run validate` — runs lint, tests, and the build together.
- To isolate a failure, run them individually: `npm run lint`,
  `npm test`, `npm run build`.

Upon completion:

- If any check fails, return to Development and repair it.
- If a failure cannot be resolved, ask for help. Never delete or disable
  a test to make it pass, unless the test is clearly broken or the
  removal is part of a deliberate refactor (and say so explicitly).
- If all checks pass, continue to Pull Request.

## Pull Request

- Open one small pull request against the default branch (`main`).
- The `validate` GitHub Actions workflow runs on the pull request; wait
  for it and resolve any failures before requesting review.
