---
name: behavior-code-tests
description: Design and review simple, readable unit/integration tests for ordinary code by testing observable behavior, user intent, contracts, and meaningful edge cases instead of implementation details, exact wording, snapshots, mocks of every call, or "every letter" assertions. Use when Codex writes, reviews, refactors, or fixes tests and must choose scenarios that catch real regressions without overfitting to the current implementation or creating clever tests nobody understands.
---

# Behavior Code Tests

## Core Rule

Test what the code promises from the outside.
Do not test private steps, exact internal calls, incidental ordering, or copied current output.
Keep tests boring and readable.
If a maintainer cannot quickly tell why the test exists, rewrite it.

Every test must answer:

1. What behavior can break?
2. Who observes the break?
3. What mutation would this test catch?

If no concrete mutation exists, delete or rewrite the test.

## Workflow

1. Read the public contract first: function name, route, command, CLI, component prop, database effect, error contract, or domain rule.
2. List behavior scenarios before writing assertions.
3. Choose the smallest test level that observes the behavior.
4. Assert state, output, domain event, persisted row, response contract, or visible UI result.
5. Use mocks only at system boundaries: network, clock, filesystem, queues, external APIs, model/provider clients.
6. Add negative and boundary cases that prove decision logic, not syntax.
7. Name the mutation each test catches in a comment, subtest name, or review note.
8. Prefer one obvious scenario per test. Use tables only when every row checks the same rule.

Read `references/scenario-selection.md` when selecting scenarios for a non-trivial module.

## Scenario Shape

Prefer:

- Valid intent succeeds.
- Invalid intent is rejected with the documented error.
- Boundary value changes behavior.
- Missing optional input uses the promised default.
- Duplicate, stale, or conflicting input is handled deterministically.
- External dependency failure returns/defer/retries as promised.
- Persistence changes only the expected records.

Avoid:

- One test per line of code.
- Asserting exact prompt text, log wording, or full JSON when only a field contract matters.
- Snapshot tests for dynamic output unless the snapshot is the product contract.
- Mocking the unit under test.
- Verifying every helper call.
- Tests that pass only because they mirror the implementation.
- Dense parameterized tests with unclear row names.
- Clever fixtures, factories, or helpers that hide the scenario.
- Broad "kitchen sink" tests that fail for many unrelated reasons.

## Unit vs Integration

Use unit tests for pure decisions, validation, mappers, policies, and branching rules.

Use integration tests when behavior depends on persistence, transactions, routes, dependency wiring, queues, auth, or cross-module contracts.

Do not replace integration behavior with deep mock choreography.

## Assertion Rules

Assert stable facts:

- Returned domain value.
- HTTP status and key response fields.
- Database row count and important columns.
- Emitted job/event type and payload contract.
- Observable side effect.
- Error class/code, not full prose unless prose is a contract.

Use partial matching for large objects.
Use exact matching only for stable public contracts.
Use plain setup data inline when it makes the behavior easier to see.
Introduce helpers only when they remove noise without hiding the important input.

## Review Gate

Reject or rewrite a test when:

- It would still pass after removing the behavior.
- It fails after harmless refactoring.
- It asserts private implementation.
- It needs more mocks than real inputs.
- It has no named mutation.
- It copies current output as expected output without explaining the contract.
- A maintainer would need to reverse-engineer fixtures or helper layers to understand the scenario.

## Output Format

When proposing tests, return:

- `Scenario`
- `Level`
- `Observable`
- `Mutation caught`

When editing tests, keep changes minimal and report verification run.
