# Commit Message Guidelines

Use the Conventional Commits format:

```text
<type>: <short imperative description>
```

Common commit types include:

- `feat`: Add a user-facing feature.
- `fix`: Correct a bug.
- `refactor`: Change code structure without changing behavior.
- `docs`: Update documentation.
- `test`: Add or update tests.
- `chore`: Make maintenance, tooling, dependency, or configuration changes.
- `build`: Change the build system or external dependencies.
- `ci`: Change continuous integration or delivery configuration.
- `perf`: Improve performance.
- `style`: Make non-functional formatting or style changes.
- `revert`: Revert an earlier commit.

Examples:

```text
feat: add account balance endpoint
fix: handle expired institution tokens
docs: document local development setup
chore: update dependency versions
```

### Atomic Commits

- Each commit should contain related changes that serve a single purpose, such as a feature subtask, issue fix, documentation update, or configuration change.
- Split large changes when they touch multiple concerns. Each commit should be independently understandable and, where practical, independently verifiable.

### Commit Message Style

- Use the present tense and imperative mood. Write `add feature`, not `added feature` or `adds feature`.
- Keep the subject concise and specific. Do not end it with a period.
- Do not add a scope. Write `feat: add endpoint`, not `feat(api): add endpoint`.
- Do not add a body unless additional context is necessary and the repository explicitly requires one.

## Guidelines for Splitting Commits

When analyzing a diff, suggest splitting commits based on these criteria:

1. **Unrelated concerns**: Changes affect unrelated parts of the codebase.
2. **Different types of changes**: Features, fixes, major refactoring, and other change types are mixed together.
3. **File patterns**: Different file categories are mixed, such as source code, documentation, tests, and configuration.
4. **Logical grouping**: Changes would be easier to understand, review, or revert separately.
5. **Size**: The change is large enough that smaller commits would make its intent and review clearer.

Do not split files that must change together for a single coherent behavior, such as an implementation and its corresponding public-interface tests.
