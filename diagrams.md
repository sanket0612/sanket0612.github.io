# Portfolio illustration concepts

The site uses original SVG illustrations based on these high-level diagrams. They describe the selected work without exposing internal architecture or source links.

```mermaid
flowchart LR
  Producer[Kafka producer] --> Outbox --> Consumer --> Sandbox[Isolated test environment]
  Context[Sandbox context] -. travels with message .-> Outbox
  Context -. contributes to routing .-> Temporal[Temporal task queue]
```

```mermaid
flowchart LR
  Checks[Grouped health checks] --> Readiness
  Checks --> Liveness
  Checks --> Ownership
  Checks --> Metrics
```

```mermaid
flowchart LR
  Build --> Checkpoint --> Rollout[ASG rollout] --> Observe
```

```mermaid
flowchart LR
  ASG[Auto Scaling Groups] -. migration work .-> Kubernetes
  Kubernetes --> Mesh[Service mesh onboarding]
  Mesh --> Ephemeral[Ephemeral development]
```

```mermaid
flowchart LR
  API --> Queue --> Payment --> Reconciliation
```

```mermaid
flowchart LR
  Interface[Insurance interface] --> API[REST API] --> Data
```
