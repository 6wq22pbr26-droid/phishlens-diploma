# PhishLens

**Design and Development of an Explainable Browser Extension for Real-Time Phishing Website Detection**

Software Engineering diploma project · SE-2422 · Supervisor: A. A. Sakhipov, PhD, Assistant Professor.

## Checkpoint — 24 October 2026

This package documents the analysis and design stage. It includes the supplied requirements and schedule, analysis of 12 survey responses, a literature review with eight scientific works, comparisons, architecture, an English interactive UI mock-up, an evaluation plan and authentic YouTrack/supervisor evidence. No trained model, installable extension, running backend or measured detection/performance result is claimed.

The supervisor's supplied 24 October message gives general positive feedback and asks for a consolidated PDF report. It is recorded without treating it as detailed technical validation. The school submission is due **24 October at 18:00 Asia/Almaty**. **PHD-1 remains due 26 October** in the preserved task plan.

## Team and planned responsibilities

| Member | GitHub | Responsibilities |
| --- | --- | --- |
| Aiym Pangerey | [aiympangerey1703](https://github.com/aiympangerey1703) | Coordination; shared frontend/backend; architecture, URL workflow, API and integration |
| Sabina Zhumagaliyeva | [6wq22pbr26-droid](https://github.com/6wq22pbr26-droid) | Shared frontend/backend; popup, settings, localization, storage and system/usability testing |
| Alibek Asylbekuly | [alibek44](https://github.com/alibek44) | Dataset/features, model training/evaluation, explanations and packaging |

Roles describe planned responsibility. Individual completed contributions require actual commits, artefacts and reviews. The YouTrack screenshots display `admin` for some ML tasks; verify that account's identity before attributing it to Alibek. Invitation acceptance and reviewer access must be verified in GitHub.

## MVP and later scope

The first MVP checks the active page URL, applies a reproducible baseline model locally where feasible, and presents risk with observable reasons in a popup. A minimal FastAPI contract is planned. An unavailable analysis must never appear as a safe verdict.

Later scope includes richer DOM/domain signals, model-explanation packaging, optional reputation checks, caching, settings and kk/ru/en localization, permitted feedback storage, Docker, CI and broader evaluation. URL-only scope and the existing task dates are preserved.

## Contents

| Path | Content |
| --- | --- |
| [Consolidated report](docs/01_PhishLens_Consolidated_Report.pdf) | Main PDF, all sections and evidence appendices |
| [YouTrack evidence](docs/02_YouTrack_Board_and_Tasks.pdf) | Separate landscape PDF of the real board and tasks |
| [Editable report](docs/00_PhishLens_Consolidated_Report.docx) | Word source |
| [Requirements](docs/01_Requirements_and_MVP_Scope.docx) | Supplied MVP with English names and review note |
| [Feedback record](docs/02_Supervisor_Feedback_Record.docx) | Faithful record of supplied supervisor messages |
| [Change record](docs/03_Team_Response_and_Change_Record.docx) | Changes made and preserved scope |
| [Complete source package](docs/PhishLens_Source_Package.zip) | Extract for the editable web report, original evidence, diagrams, prototype and task plan |
| `docs/sources.json` / `docs/requirements.json` | Source catalogue and requirements |
| `docs/evidence/` | Original survey, YouTrack and supervisor screenshots |
| `diagrams/` | Editable Mermaid diagrams and SVG design views |
| UI prototype inside the source ZIP | English, manually selected demonstration states |
| `management/task-plan.json` | Preserved 19-task schedule; not a live export |
| `tests/manual-checklist.txt` | Interface and evidence review checks |

PDF and Word files are directly available under docs. The complete directory structure for the prototype, diagrams, evidence and editable web report is preserved inside docs/PhishLens_Source_Package.zip; extract the ZIP before opening those files. The report records the evidence status at assembly time; live access and actual peer review remain to be verified.

## Open the prototype

Download the repository/package and open `prototype/index.html` in a browser. No server, dependency installation or account is needed. Select Loading, Low risk, Warning and Unavailable. Expand technical details and try the unavailable-state retry control. The prototype sends no network requests and provides no phishing protection.

Production installation and model reproduction instructions will be added when those components exist. Candidate technologies are TypeScript/Manifest V3, Python/scikit-learn, ONNX Runtime Web and FastAPI; their alternatives and validation gates are in the report.

## Research status and limitations

The survey has 12 responses; Q7 has 11. Results are exploratory, based on screenshots without a raw export. Q12 contains contradictory exclusive-option selections and is not used to confidently rank barriers. Interest in the idea is not product validation.

Records of the required 3–5 user discussions or a substantive client agreement were not supplied. The survey does not automatically replace that evidence. No interview records, user tests, model metrics, teammate reviews or contributions have been invented. The documents were assembled with AI assistance and require the team's actual ownership and review.

## Links

- [Repository](https://github.com/6wq22pbr26-droid/phishlens-diploma)
- [YouTrack instance](https://aiympangerey1703.youtrack.cloud) — project: Explainable Phishing Detection (PHD); exact project/board link and access must be checked in the service.
- [English student survey](https://docs.google.com/forms/d/e/1FAIpQLSeKItS51CarKIaIW3Mt9TAiw5Keploe_ShI60XnwVSWySVP2g/viewform)

## Workflow and access

Use the actual PHD task ID in branches, commits and pull requests. Another member reviews substantive changes; link the PR to YouTrack. Mark work Done only when its acceptance conditions are met. Create the submission tag only on the reviewed commit. Preserve real authorship and dates.

Before submission, verify that the supervisor and commission can open the private repository and YouTrack board, and that Aiym and Alibek have accepted invitations. The submitted screenshots show 18 Backlog tasks and PHD-1 in Review; they are historical snapshots, not proof of later completion.

## Data handling

Do not commit passwords, API keys, identifiable respondent records or browsing histories. Local processing is the preferred design. External URL/domain checks require documented consent and data flow. Dataset licences, label mapping, duplicate/domain leakage and online feature availability must be checked before training. F1 ≥ 0.90 and local latency ≤ 200 ms are proposed targets, not achieved results.
