# 03 · Research Methodology

[← Back to README](../README.md) · [Documentation index](README.md)

## Study Design

The project used an iterative research-and-development methodology: literature review, dataset characterization, preprocessing, model design, explainability integration, web-system implementation, and multi-level evaluation.

```mermaid
flowchart LR
  A[Literature & gap analysis] --> B[Dataset characterization]
  B --> C[Preprocessing & sampling]
  C --> D[Model development]
  D --> E[XAI & uncertainty]
  E --> F[System integration]
  F --> G[Quantitative testing]
  G --> H[Simulated UAT]
  H --> I[Limitations & future work]
```

## Dataset Boundary

The academic study used the HER2-IHC-40x histopathology image dataset associated with University of Malaya Medical Centre. The report describes whole-slide images, expert-annotated regions, and extracted patches across four HER2 categories.

| Reported split | Patches |
| --- | ---: |
| Training | 4,796 |
| Validation | 533 |
| Testing | 1,628 |

The public repository does **not** contain the dataset, raw patches, annotations, slide identifiers, or derived training files.

## Preprocessing Strategy

- Whole-slide access and resolution normalization.
- Overlapping `256 × 256` patch extraction.
- Tissue filtering to remove mostly blank regions.
- RGB normalization and color/geometry augmentation.
- Whole-slide-oriented splitting to reduce leakage risk.
- Stratification and oversampling to address class imbalance.

## Evaluation Strategy

The model was assessed using precision, recall, F1, confusion patterns, and precision-recall behavior. The integrated platform was evaluated with unit tests, cross-module integration tests, and simulated doctor, nurse, and administrator acceptance scenarios.

## Reproducibility Limits

The public case study provides methodological transparency without releasing restricted data, implementation code, trained model artifacts, or exact operational credentials. Reproducing the reported results requires authorized dataset access and an independently reviewed experimental protocol.
