---
name: me-to-spec
description: "Turn the current conversation into a spec written to a local spec.md, then open it in Plannotator for annotation."
disable-model-invocation: true
---

This skill takes the current conversation context and codebase understanding and produces a spec. Do NOT interview the user; just synthesize what you already know.

## Process

1. Explore the repo to understand the current state of the codebase, if you haven't already. Use the project's domain glossary vocabulary throughout the spec, and respect any ADRs in the area you're touching.

2. Sketch out the seams at which you're going to test the feature. Existing seams should be preferred to new ones. Use the highest seam possible. If new seams are needed, propose them at the highest point you can. The fewer seams across the codebase, the better - the ideal number is one.

   Check with the user that these seams match their expectations.

3. Write the spec using the template below to `spec.md` at the repo root.

4. Run `plannotator annotate spec.md` so the user can annotate and refine the spec in the browser. Block until they submit feedback or approve, then address any returned annotations inline in `spec.md`.

<spec-template>

## Problem Statement

The problem that the user is facing, from the user's perspective.

## Solution

The solution to the problem, from the user's perspective.

## User Stories

A numbered list of user stories, each in the format:

1. As an <actor>, I want a <feature>, so that <benefit>

<user-story-example>
1. As a mobile bank customer, I want to see balance on my accounts, so that I can make better informed decisions about my spending
</user-story-example>

Cover every aspect of the behaviour this change **introduces or alters**, exhaustively.

- **Genuine stories only.** Each <feature> is a concrete capability the actor uses or observes and each <benefit> is the value they get. A structural or architecture goal ("so that future views are easy to add", "so the nav is ready for more tabs") is not a user story even with a benefit clause; record those under Implementation Decisions.
- **New behaviour only.** Behaviour that already exists and is merely relocated or left unchanged does not belong here. Record it under a "Preserved behaviour" note in Further Notes so it is not restated as new work.

## Architecture (optional)

Include a diagram only where one explains an aspect that prose and the other diagrams cannot. Prefer the highest-level view that lands the point; drop to a lower-level diagram only for a genuinely complex area. Match the standard diagram type to the aspect - class for structure, sequence for interactions, state machine for lifecycles, activity for branching flows.

## Implementation Decisions

A list of implementation decisions that were made. This can include:

- The modules that will be built/modified
- The interfaces of those modules that will be modified
- Technical clarifications from the developer
- Architectural decisions
- Schema changes
- API contracts
- Specific interactions

Do NOT include specific file paths or code snippets. They may end up being outdated very quickly.

Exception: if a prototype produced a snippet that encodes a decision more precisely than prose can (state machine, reducer, schema, type shape), inline it within the relevant decision and note briefly that it came from a prototype. Trim to the decision-rich parts, not a working demo, just the important bits.

## Testing Decisions

A list of testing decisions that were made. Include:

- A description of what makes a good test (only test external behavior, not implementation details)
- Which modules will be tested
- Prior art for the tests (i.e. similar types of tests in the codebase)

## Out of Scope

A description of the things that are out of scope for this spec.

## Further Notes

Any further notes about the feature.

</spec-template>
