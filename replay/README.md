# Replay Verification

Replay verification is the procedure used to confirm that a declared artifact evaluation can be reproduced from the same evidence set.

## Purpose

Replay verification answers a simple question:

Can the same artifact set produce the same recorded decision?

## Canonical Inputs

A replay-verifiable evaluation should preserve:

- source artifact
- artifact SHA256
- decision receipt
- decision receipt SHA256
- deterministic decision fields

## Canonical Example

The current reference example comes from the artifact engine successful run:

`~/witness_artifact_engine/receipts/RUN_20260315T083740Z`

## Expected Result

For a valid replay:

- artifact hash matches recorded hash
- decision receipt hash matches recorded hash
- kernel decision remains the same
- run remains admissible under the recorded evidence

## Failure Modes

Replay should fail if:

- artifact bytes differ
- decision receipt bytes differ
- required witness artifacts are missing
- deterministic decision fields do not match
