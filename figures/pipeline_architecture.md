# Continuation Control Pipeline

```mermaid
flowchart TD
    A[Declared Process] --> B[Artifact Capture]
    B --> C[Witness Chain]
    C --> D[Continuation Kernel]
    D --> E[HALT]
    D --> F[INCOMPLETE]
    D --> G[PASS]

## Diagram 2: decision structure

```bash
cat > figures/kernel_decision_structure.md <<'EOF'
# Continuation Kernel Decision Structure

```mermaid
flowchart TD
    A[Artifact Set] --> B{Witness Chain Valid?}
    B -- No --> H[HALT]
    B -- Yes --> C{Evidence Complete?}
    C -- No --> I[INCOMPLETE]
    C -- Yes --> D{Continuation Admissible?}
    D -- No --> J[HALT]
    D -- Yes --> K[PASS]
