# Scenario Selection

Use this checklist before writing unit or integration tests.

## Build The Scenario List

Start from behavior, not code paths:

1. Main user intent.
2. Permission or precondition failure.
3. Missing, empty, duplicate, stale, or conflicting input.
4. Boundary values.
5. External boundary failure.
6. Persistence or transaction effect.
7. Idempotency or retry behavior if the operation can repeat.

Keep only scenarios with a visible consequence.
Prefer the fewest scenarios that explain the behavior.
Do not add edge cases just because they are possible.

## Pick Test Level

Use unit when one module can prove the rule with plain inputs and outputs.

Use integration when the risk is wiring, database behavior, transaction boundaries, auth, middleware, serialization, background jobs, or provider adapters.

Use one integration test for the contract and unit tests for dense decision tables.
Avoid dense tables unless the rule is simple and every row has a clear name.

## Mutation Examples

Good tests catch mutations like:

- Flip `>` to `>=`.
- Remove authorization guard.
- Ignore missing input.
- Swap default value.
- Persist the wrong status.
- Drop transaction rollback.
- Return success on provider failure.
- Use wrong tenant/user scope.
- Process duplicates twice.

Weak tests only catch:

- Renamed helper.
- Reordered internal calls.
- Different equivalent formatting.
- Refactored private function layout.

## Assertion Examples

Prefer partial contract assertions:

```text
status = 201
body.data.id exists
body.data.status = "pending"
database has one matching row for current tenant
```

Avoid full-object assertions when unrelated fields can change.

## AI-Agent Reminder

Do not maximize test count.
Maximize regression detection per test.

One strong behavior test is better than five implementation-shaped tests.
One clear test is better than one clever test.
