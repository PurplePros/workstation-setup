# Pull Request Best Practices

This guide outlines the standard practices for authoring pull requests (PRs).

## 1. Keep PRs Small and Focused
* Aim for fewer than 500 lines of code. The ideal is 200-300 lines
* Address only one issue, feature, or bug per PR

## 2. Craft Clear Titles
* Describe imperatively what the PRs addresses on a high level
* Use the Conventional Commits format to describe the type of PR (i.e., `feat: add JWT validation to backend API`)

## 3. Craft Clear Descriptions

Every description has these sections, in this order:

### What

Describe the user-facing value delivered by the change, not a list of implementation details. Explain the capability or experience now available. For example, a user app that integrates Plaid should say that users can add new accounts and sync existing accounts through the full Plaid integration.

### Why

Describe the user or product value motivating the change. Explain the problem this solves and why the capability matters. Do not use this section as a second implementation summary or merely restate `What`.

### Design decisions (optional)

Include this section only when the work involved a major design choice or meaningful tradeoff. State the approach taken, the notable alternative, and why this approach was chosen. Omit the section for routine implementation details.

### Tests

Use this format:

```markdown
## Tests

:white-check-mark: Added unit tests
:white-circle: Tested E2E

### E2E scenarios
- [ ] A user can ... and sees ...
- [ ] A user can ... and sees ...
```

Include `:white-check-mark: Added unit tests` only when the PR adds unit tests. Always include `:white-circle: Tested E2E` as a placeholder for the user to update after verification. Fill in each E2E checkbox with a user flow and its expected outcome. State any intentional coverage boundary when an applicable scenario cannot be verified, and explain why. The user adds screenshots and other verification details under the relevant scenario.

### 4. Run CI Checks Locally
* Execute linting, formatting, and unit test suites locally before pushing your branch.
* Fix all warnings and errors on your machine to ensure a green CI pipeline on the first run.
* Utilize local automation tools (like Git hooks) to prevent committing non-compliant code.
