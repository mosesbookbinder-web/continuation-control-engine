# Deterministic Replay Specification

## Definition

Deterministic replay is the process of re-evaluating a preserved artifact set and confirming that the same admissibility result is obtained under the same evidence.

## Replay Contract

A replay-verifiable continuation decision requires the following artifacts:

1. artifact payload
2. artifact SHA256
3. decision receipt
4. decision receipt SHA256
5. stable decision fields

## Stable Decision Fields

At minimum, the following fields must remain consistent:

- decision
- kernel_decision
- submission_readiness
- artifact_sha256
- decision_receipt_sha256
- kernel_gate_vector

## Reference Example

Reference run:

`RUN_20260315T083740Z`

Reference artifact SHA256:

`0aa59f775cd41ce157d3d23e53fad000922e8c7a5e4a93b099646bfb76304c1f`

Reference decision receipt SHA256:

`74bf878306a01f7da3e9715ce4d57f94293ecf711fb374d4bd350b5c7f057f87`

Reference decision:

`PASS`

## Verification Procedure

1. locate the preserved artifact
2. compute SHA256 of the artifact
3. compare against recorded artifact SHA256
4. locate the decision receipt
5. compute SHA256 of the decision receipt
6. compare against recorded receipt SHA256
7. inspect stable decision fields
8. confirm that replay status is unchanged

## Decision Semantics

Replay outcomes should be interpreted under strict precedence:

HALT > INCOMPLETE > PASS

A mismatch in required replay artifacts should be treated as a replay failure and should not be promoted to PASS.

## Principle

No replay, no trust.
