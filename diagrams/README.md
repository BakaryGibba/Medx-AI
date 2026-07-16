# Diagram Library

[← Back to the Medx AI case study](../README.md)

The `.mmd` files are editable Mermaid sources. GitHub renders the corresponding Mermaid blocks directly inside the case-study documents; PNG exports are optional.

| Diagram | Purpose | Used in |
| --- | --- | --- |
| [architecture.mmd](architecture.mmd) | System layers, users, services, and storage | [System Architecture](../docs/07-system-architecture.md) |
| [diagnostic-workflow.mmd](diagnostic-workflow.mmd) | End-to-end clinical workflow | [Clinical Workflows](../docs/09-clinical-workflows.md) |
| [ai-pipeline.mmd](ai-pipeline.mmd) | Preprocessing, ensemble prediction, uncertainty, and XAI | [AI Model](../docs/04-ai-model.md) |
| [llm-workflow.mmd](llm-workflow.mmd) | Context assembly, generation, validation, and review | [LLM Recommendations](../docs/06-llm-recommendations.md) |
| [clinical-sequence.mmd](clinical-sequence.mmd) | Interaction sequence across users and AI services | [Clinical Workflows](../docs/09-clinical-workflows.md) |
| [recommendation-state.mmd](recommendation-state.mmd) | Recommendation lifecycle and authority boundary | [Clinical Workflows](../docs/09-clinical-workflows.md) |
| [data-model.mmd](data-model.mmd) | Core clinical entities and traceability relationships | [Data & System Design](../docs/08-data-and-system-design.md) |
| [validation-roadmap.mmd](validation-roadmap.mmd) | Research-to-clinical validation stages | [Future Work](../docs/14-future-work.md) |

## Optional Export

With Mermaid CLI installed:

```powershell
mmdc -i diagrams/architecture.mmd -o diagrams/architecture.png -b transparent
```

The `.mmd` files do not automatically become PNGs on GitHub. They remain source files; diagrams embedded in Markdown render automatically. Export PNGs only for presentations or platforms without Mermaid support.
