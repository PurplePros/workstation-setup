# Software engineering principles

## Ownership

Put a constant on the class when that class is its only consumer. Use a module-level constant only when multiple independent consumers share it. Share a constant across modules only when its consumers share the same concept: a coincidence of value is not a reason to merge. Two constants that happen to hold the same number but represent distinct domain concerns at different layers stay independent - coupling them makes both harder to evolve.

## Dependencies

Inject collaborators through the public constructor or method boundary. Compose and wire concrete dependencies at a higher-level entry point so the class owns its behavior, not object construction, and tests can supply meaningful collaborators.

## Data types

Methods that answer questions about a type's own state, or that produce an instance from a set of inputs, belong on the type as a property or classmethod. A free function that takes a type's fields as its parameters is a displaced method; move it onto the type.

## Branches

Treat an `if`/`else` that selects behavior as a value-abstraction prompt. When the alternatives represent distinct concepts with their own behavior, model them as separate classes behind a shared interface. Keep a conditional when it is the clearest representation of simple, local control flow.
