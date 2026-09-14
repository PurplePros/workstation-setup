# ~/.agents/AGENTS.md

## Working agreements
1. Never using the em dash "—". Use plain dash "-" instead
2. When making technical decisions, do not give much weight to development cost. Instead, prefer quality, simplicity, robustness, scalability, and long-term maintainability
3. Keep code comments clear. Good comments do not duplicate the code, explains unidiomatic code, links to external references if helpful, and explains the intent and the why.
4. Unit tests must always test the public interface, not the internal implementation details
5. Never reference tickets/issues (e.g. "PUR-7", "fixes #123") in code comments. Comments should stand on their own without the tracker; sequencing/ownership info belongs in the PR description or commit message, not the code. Exception: if the *why* behind unidiomatic code or a design decision is itself important to note, explain the why directly in the comment - don't just cite the ticket as a stand-in for the reasoning.
6. All communications (chat responses, PR descriptions, commit messages, code comments) must be concise. Cut restatement, hedging, and anything the reader can already see for themselves.

## Pull request creation
When you are creating a pull request, read ~/PULL_REQUESTS.md to understand how to create pull requests

## Commit messages
When you are creating a commit message, read ~/COMMIT_MESSAGES.md to understand how to create commit messages

## Software engineering principles
When designing, reviewing, or refactoring production code, read ~/OPINIONS.md and apply its directives.

## Voice and tone
When writing on my behalf (pull requests, commit messages, Slack messages, or any external communication), read ~/VOICE.md and write in my voice.
