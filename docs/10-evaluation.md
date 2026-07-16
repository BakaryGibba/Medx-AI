# 10 · Evaluation

[← Back to README](../README.md) · [Documentation index](README.md)

## Model Results

The final report documents approximately 96% weighted accuracy for the ensemble in its controlled evaluation setting.

| Class | Precision | Recall | F1 | Average precision |
| --- | ---: | ---: | ---: | ---: |
| HER2 `0` | 0.99 | 0.93 | 0.96 | 0.994 |
| HER2 `1+` | 0.87 | 0.96 | 0.92 | 0.950 |
| HER2 `2+` | 0.87 | 0.95 | 0.91 | 0.953 |
| HER2 `3+` | 1.00 | 0.98 | 0.99 | 0.999 |

The strongest portfolio insight is not the aggregate score alone. Intermediate `1+` and `2+` cases are clinically important and harder to separate, so per-class behavior and uncertainty routing deserve more attention than a single accuracy value.

## System Verification

| Evaluation layer | Reported tests | Passed |
| --- | ---: | ---: |
| Unit | 52 | 52 |
| Integration | 66 | 66 |
| UAT scenarios | 36 | 36 |
| **Total** | **154** | **154** |

Integration coverage included the complete diagnosis flow, access control, soft deletion, token refresh, file handling, OCR, LLM integration, activity logging, and notifications.

## Simulated UAT

| Criterion | Reported score / 5 |
| --- | ---: |
| Navigation | 4.6 |
| Workflow logic | 4.5 |
| Prediction clarity | 4.7 |
| Grad-CAM usefulness | 4.8 |
| Recommendation quality | 4.5 |
| Disclaimer visibility | 4.9 |

## How to Interpret the Evidence

> [!CAUTION]
> Passing software tests demonstrates implementation consistency, not clinical validity. Simulated UAT demonstrates usability with the tested participants, not safety across real hospitals. The reported model metrics require independent reproduction and cross-site validation.

The report's per-class support values do not sum to the earlier stated test-patch total. This does not invalidate the portfolio summary, but the evaluation cohort and filtering steps should be reconciled before journal submission or independent replication.

## Evaluation Gaps

- External and prospective clinical validation.
- Confidence calibration and decision-curve analysis.
- Patient-level subgroup and fairness analysis.
- Scanner, stain, and institution domain-shift testing.
- Independent pathology review of explanation quality.
- LLM factuality, citation, and guideline-version benchmarks.
- A single reproducible evaluation manifest reconciling split sizes, exclusions, and per-class support.
