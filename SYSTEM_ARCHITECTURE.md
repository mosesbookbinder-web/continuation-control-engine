# System Architecture

## Pipeline

Declared Process  
↓  
Artifact Capture  
↓  
Witness Chain  
↓  
Continuation Kernel  
↓  
HALT / INCOMPLETE / PASS

## Decision Rule

Continuation Control uses strict decision precedence:

HALT > INCOMPLETE > PASS

## Architecture Layers

### 1. Declared Process
A process, workflow, or evaluation declares its intention to execute.

### 2. Artifact Capture
Artifacts are collected from the declared process. These may include text, logs, files, inputs, outputs, or structured records.

### 3. Witness Chain
Artifacts are linked into a reproducible witness structure through stable ordering and cryptographic hashing.

### 4. Continuation Kernel
The kernel evaluates whether continuation is admissible under replay-verifiable evidence.

### 5. Decision
Exactly one decision is emitted:

- HALT
- INCOMPLETE
- PASS

## Kernel Logic

The kernel evaluates three structural questions:

1. Is the artifact chain valid?
2. Is the evidence complete?
3. Is continuation admissible?

## Conceptual Model

Continuation Control exists at the intersection of:

- replay-verifiable evidence
- deterministic evaluation
- continuation authority

## Output Principle

No artifact, no claim.  
No replay, no trust.  
No authority, no continuation.
