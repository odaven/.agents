## Git

- Never push directly to `main`, `master`, or `develop`.
- Branch names: `feat/add-user-search`, `fix/null-pointer-on-login`, `refactor/simplify-cache`
- One logical change per commit. Don't mix refactoring with functional changes.
- Use Conventional Commits for commit messages and PR titles: `type(scope): description` or `type: description`
  - Example: `feat(auth): add JWT validation`, `fix(api): handle null responses`
- Never merge PRs or close issues without explicit instruction.
- Never rewrite shared history or force-push unless explicitly requested.
