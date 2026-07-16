# 01 · Executive Summary

[← Back to README](../README.md) · [Documentation index](README.md)

## Overview

Medx AI is a final-year research and engineering project investigating explainable, clinician-supervised AI for HER2 assessment in breast cancer histopathology. It unifies classification, uncertainty handling, visual explanation, contextual recommendation drafting, role-based workflows, and auditability within a web prototype.

The project asks a broader systems question: **how can an accurate research model become a useful and responsible clinical decision-support workflow?**

## Academic Context

| Item | Detail |
| --- | --- |
| Degree | Bachelor of Computer Science (Honours) |
| Institution | Albukhary International University |
| Completion | January 2026 |
| Team | Bakary Gibba, Md Rashidul Islam, Faisal Rafat Faisal Khrisan |
| Supervisor | Professor Dr. Zurinahni Binti Zainol |
| Bakary's primary role | Model development and explainable AI |

## System Contribution

The prototype connects three layers that are often evaluated separately:

1. **Prediction:** four-class HER2 status estimation with confidence and class probabilities.
2. **Interpretation:** Grad-CAM and uncertainty signals support scrutiny rather than blind acceptance.
3. **Clinical workflow:** LLM-generated drafts remain pending until explicitly reviewed by a clinician.

## Reported Outcomes

- Approximately 96% weighted classification accuracy in the documented test setting.
- Strong reported recall for difficult `1+` and `2+` classes: 0.96 and 0.95.
- 154 reported unit, integration, and acceptance tests passed.
- Average reported user satisfaction of 4.5/5 in simulated role-based UAT.

> [!WARNING]
> These outcomes describe an academic prototype evaluated on a specific dataset and simulated workflows. They do not establish clinical efficacy, regulatory compliance, or generalization to other institutions.

## Portfolio Value

Medx AI demonstrates applied machine learning, computer vision, explainable AI, LLM orchestration, safety-oriented design, multidisciplinary communication, and full-system evaluation. The repository intentionally presents those decisions without publishing source code, data, patient material, model weights, or the private dissertation.
