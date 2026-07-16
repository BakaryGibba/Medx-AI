# 14 · Future Work

[← Back to README](../README.md) · [Documentation index](README.md)

## Research Priorities

1. Validate on multiple institutions, scanners, staining protocols, and demographic groups.
2. Compare the ensemble with calibrated deep and foundation-model baselines under identical splits.
3. Conduct independent pathology review of prediction errors and explanation faithfulness.
4. Add calibration, selective prediction, decision-curve analysis, and subgroup evaluation.
5. Reproduce all claims through a preregistered and auditable experiment pipeline.

## Clinical AI Improvements

- Ground LLM responses in versioned oncology guidelines with verifiable citations.
- Test hallucination, omission, prompt injection, and contradictory-context scenarios.
- Host sensitive AI services on-premise where governance requires it.
- Separate research recommendations from institution-approved clinical pathways.
- Measure automation bias and reviewer disagreement.

## Engineering Improvements

- Asynchronous queues for inference, OCR, and report generation.
- Encrypted object storage with lifecycle and access policies.
- Model registry with approval, rollback, drift monitoring, and lineage.
- DICOM/PACS interoperability and standards-based clinical integration.
- Security review, threat modeling, penetration testing, and disaster recovery.
- Production observability for latency, failures, drift, and audit anomalies.

## Validation Roadmap

```mermaid
flowchart LR
  A[Academic prototype] --> B[Reproducible retrospective study]
  B --> C[External multi-site validation]
  C --> D[Silent prospective evaluation]
  D --> E[Human factors & clinical safety study]
  E --> F[Regulatory and institutional review]
  F --> G[Monitored clinical deployment]
```

The project currently sits at the first stage. Progress should be evidence-led, multidisciplinary, and governed by clinical and regulatory experts.
