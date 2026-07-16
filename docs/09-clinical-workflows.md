# 09 · Clinical Workflows

[← Back to README](../README.md) · [Documentation index](README.md)

## Role Separation

| Role | Primary responsibilities |
| --- | --- |
| Nurse | Register and maintain patient records |
| Doctor | Create cases, run analysis, inspect explanations, review recommendations, finalize reports |
| Administrator | Manage users, archives, platform activity, and operational visibility |

## Diagnostic Sequence

```mermaid
sequenceDiagram
  actor Nurse
  actor Doctor
  participant App as Medx AI
  participant Model as HER2 + XAI
  participant LLM as Recommendation service

  Nurse->>App: Register or update patient
  Doctor->>App: Create diagnostic case
  Doctor->>App: Upload histopathology image
  App->>App: Validate image quality and distribution
  App->>Model: Run prediction and explanation
  Model-->>App: Class, probabilities, uncertainty, Grad-CAM
  Doctor->>App: Inspect result and add context
  App->>LLM: Request structured draft
  LLM-->>App: Assessment, follow-up, risk mitigation
  App-->>Doctor: Mark recommendation pending review
  Doctor->>App: Accept, reject, or investigate
  App-->>Doctor: Generate traceable report from approved records
```

## Recommendation State

```mermaid
stateDiagram-v2
  [*] --> NotGenerated
  NotGenerated --> Draft: generate
  Draft --> PendingReview: validate structure
  PendingReview --> Saved: clinician accepts
  PendingReview --> Discarded: clinician rejects
  PendingReview --> Draft: regenerate
  Saved --> Reported: include in report
  Discarded --> [*]
  Reported --> [*]
```

## UX Principle

The interface surfaces uncertainty, risk, explanation, and review actions in the same workflow. This reduces the chance that an AI output is mistaken for a finalized clinical decision simply because it appears polished or authoritative.

See the [workflow screenshots](../screenshots/README.md) for implemented evidence.
