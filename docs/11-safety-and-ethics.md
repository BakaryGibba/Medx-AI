# 11 · Safety & Ethics

[← Back to README](../README.md) · [Documentation index](README.md)

## Safety Position

Medx AI is framed as decision support. The system can assist with evidence organization and workflow consistency, but medical responsibility remains with qualified clinicians and institutional governance.

## Safety Layers

| Layer | Mechanism | Residual risk |
| --- | --- | --- |
| Input | Blank, blur, stain, and distribution checks | Valid-looking images may still be unsuitable |
| Prediction | Probabilities and entropy | Confidence may be miscalibrated under domain shift |
| Explanation | Grad-CAM beside original image | Visual plausibility can be mistaken for causal validity |
| Generation | Structured prompts and conservative fallback | LLMs can still hallucinate or use outdated guidance |
| Workflow | Pending review and explicit accept/reject | Reviewers may anchor on AI suggestions |
| Governance | Roles, activity logs, version references | Technical logging alone does not create regulatory compliance |

## Ethical Commitments

- Human oversight for every recommendation used in a report.
- Clear distinction between prediction, recommendation draft, and clinical decision.
- Data minimization and restricted release of medical material.
- Traceability from output back to image, case, model version, and reviewer.
- Transparent communication of evaluation limitations.
- No claim of clinical deployment readiness.

## Privacy

A production system would require formal consent, lawful processing, data-retention policies, encryption, access review, incident response, vendor agreements, and institution-specific compliance assessment. External LLM and OCR services would require particular scrutiny because uploaded history may contain sensitive information.

## Bias and Equity

Performance can vary across institutions, populations, laboratory practices, scanners, and staining conditions. A high aggregate score can conceal clinically meaningful subgroup failures. Future evaluation should predefine subgroup metrics and involve diverse clinical sites.

## Intended Impact

The project aligns with responsible digital-health goals by exploring lower-compute classification, explanation, and review-oriented workflows. Social value depends on validated safety and equitable performance, not simply on making AI available.
