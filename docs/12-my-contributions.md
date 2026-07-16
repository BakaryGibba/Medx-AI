# 12 · My Contributions

[← Back to README](../README.md) · [Documentation index](README.md)

## Ownership Boundary

The project report records the following team distribution:

| Workstream | Primary owner |
| --- | --- |
| Model development and explainable AI | **Bakary Gibba** |
| Frontend development | Md Rashidul Islam |
| Backend development | Faisal Rafat Faisal Khrisan |
| Documentation | All team members |
| System testing | All team members |

This case study preserves that boundary so reviewers can distinguish individual depth from collaborative system outcomes.

## Bakary's Technical Contributions

### Model Development

- Designed the four-class HER2 prediction workflow.
- Developed the image preprocessing and feature pipeline.
- Evaluated Random Forest, Logistic Regression, and SVM behavior.
- Combined classifier probabilities through a soft-voting ensemble.
- Addressed class imbalance and reviewed per-class performance.
- Packaged prediction outputs for integration: class, confidence, probability distribution, and model identity.

### Explainable and Safer AI

- Integrated Grad-CAM visual explanations into the prediction workflow.
- Connected heatmap output to clinician-facing interpretation.
- Added quality and distribution checks before inference.
- Used uncertainty behavior to defer borderline outputs rather than always forcing a class.
- Evaluated attention patterns and ambiguous HER2 categories.

### Collaborative Contributions

- Contributed AI contracts and artifacts needed by frontend and backend integration.
- Participated in end-to-end testing and defect resolution.
- Co-authored project documentation, methodology, discussion, and limitations.

## Engineering Evidence

The strongest evidence of the contribution is the complete path from input validation to ensemble prediction, uncertainty, Grad-CAM output, and clinician review. It demonstrates model engineering in a product context rather than an isolated notebook experiment.

## Reflection

The project strengthened my interest in explainable, human-centered AI. It also showed me that responsible medical AI requires collaboration across modeling, software engineering, clinical expertise, governance, and evaluation.
