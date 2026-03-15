# Artifact Engine

The artifact engine provides the runnable interface for Continuation Control artifact evaluation.

## Source Repository

The current implementation lives in:

`~/witness_artifact_engine`

GitHub repository:
`mosesbookbinder-web/witness-artifact-engine`

## Canonical Successful Run

Reference run:

`receipts/RUN_20260315T083740Z`

This run demonstrates:

- artifact ingestion
- deterministic evaluation
- decision receipt emission
- witness bundle hashing

## Expected Decision

Decision: PASS  
Kernel decision: PASS  
Submission readiness: READY

## Canonical Receipt Fields

- artifact_path
- artifact_sha256
- decision_receipt_path
- decision_receipt_sha256_path
- decision_receipt_sha256
- kernel_gate_vector

## Example Artifact

See:

`../examples/example_artifact.txt`

This example is the minimal repeatable artifact used to demonstrate receipt generation and deterministic PASS behavior.
