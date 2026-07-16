# 13 · Challenges

[← Back to README](../README.md) · [Documentation index](README.md)

## 1. Ambiguous HER2 Classes

The `1+` and `2+` categories are harder to separate and more consequential than an aggregate accuracy number suggests. The team used class balancing, per-class metrics, full probability displays, and uncertainty-aware review to make this difficulty visible.

## 2. Limited and Imbalanced Data

Medical data is expensive to annotate and difficult to share. The ensemble strategy reduced compute requirements, while augmentation and oversampling addressed imbalance. The unresolved trade-off is external generalization.

## 3. Explaining Heterogeneous Models

Visual explanation is most natural for spatial deep models, while the classification strategy used engineered features and classical learners. The project used a surrogate deep model for Grad-CAM visualization, which supports spatial inspection but does not directly explain the ensemble. Explanation faithfulness remains a central research limitation.

## 4. Preventing Unsafe Automation

The system needed to avoid turning a prediction or fluent LLM output into an automatic decision. Pending-review states, uncertainty deferral, explicit disclaimers, and clinician acceptance were treated as architecture rather than copywriting.

## 5. Converting Research Into Workflow

A useful prototype required more than model inference: identity, roles, patient records, cases, documents, storage, model versions, notifications, audits, recommendation lifecycle, and reports all had to remain coherent.

## 6. External AI Providers

Provider APIs accelerated LLM and OCR experimentation but introduced privacy, latency, availability, and reproducibility risks. Provider fallback improves uptime but does not solve data-governance concerns.

## Lessons

- Evaluate the difficult class, not only the average.
- Make uncertainty actionable in the user interface.
- Treat explanation as contestable evidence.
- Keep generated language behind an explicit authority boundary.
- Document what remains unvalidated as carefully as what worked.
