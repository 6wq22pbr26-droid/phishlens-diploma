# PhishLens

**Design and Development of an Explainable Browser Extension for Real-Time Phishing Website Detection**

Software Engineering diploma project, group SE-2422.  
Supervisor: A. A. Sakhipov, PhD, Assistant Professor.

## Problem and aim

Users can encounter deceptive websites while browsing and may struggle to recognise phishing indicators or interpret security warnings. PhishLens aims to assess phishing indicators on the current webpage and present understandable reasons for its risk assessment.

The proposed audience includes university students and other everyday internet users. The current research survey focuses on university students aged 18 or older. User needs and assumptions will be refined using collected evidence.

## Team and responsibilities

| Team member | GitHub | Planned responsibilities |
| --- | --- | --- |
| Aiym Pangerey | [aiympangerey1703](https://github.com/aiympangerey1703) | Team coordination; frontend and backend development jointly with Sabina; architecture, analysis flow, risk display, URL-check API and integration. |
| Sabina Zhumagaliyeva | [6wq22pbr26-droid](https://github.com/6wq22pbr26-droid) | Frontend and backend development jointly with Aiym; user scenarios, UI prototype, settings, trusted sites, feedback, localisation, storage, reputation integrations and user testing. |
| Alibek Asylbekuly | [alibek44](https://github.com/alibek44) | Dataset assessment, feature engineering, model training and comparison, evaluation, explainability and model export for integration. |

Each task will have one accountable assignee. These responsibilities describe planned work; individual contributions must be evidenced by actual commits, deliverables and reviews.

## Current status — 23 October 2026

The project is in the analysis and design stage.

- The repository has been created. Invitations were sent to Aiym and Alibek on 22 October; their acceptance has not yet been verified.
- An English multiple-choice survey has been published. Response analysis is pending.
- An AI-assisted local draft package contains analysis, requirements, diagrams, a UI prototype and an evaluation plan. It requires team review, updated role assignments and upload to this repository.
- The team is configuring YouTrack. The final project/board link and task identifiers are pending.
- User-discussion evidence and substantive supervisor feedback have not yet been incorporated.
- No trained model, deployable browser extension or backend service is available. No model-quality or runtime-performance results are claimed.

The initial report PDFs are review drafts with outdated role assignments and must not be treated as final submission documents.

## Scope and expected outcomes

The planned MVP includes webpage URL/DOM feature analysis, a risk indication with explanations, trusted-site settings and optional reputation checks. Planned supporting features include feedback and Kazakh, Russian and English interface localisation, subject to agreed scope and available time.

Expected outcomes are an installable browser extension, documented supporting services, a reproducible model evaluation and a report on usability, performance and limitations. The tool will provide risk indications, not a guarantee that a website is safe.

A complete application is not required for the 24 October checkpoint. That checkpoint covers analysis, design, planning, traceable contributions and supervisor review.

## Proposed technologies

| Component | Proposed technologies | Decision status |
| --- | --- | --- |
| Browser extension | TypeScript, Manifest V3, Chrome/Edge | Planned; compatibility testing pending |
| Model development | Python, scikit-learn | Planned; dataset and model comparison pending |
| Local inference | ONNX Runtime Web | Candidate; export compatibility, size and latency must be evaluated |
| Backend | FastAPI | Proposed; justification and implementation pending |
| Storage | PostgreSQL | Proposed; final data requirements and privacy review pending |
| Packaging and checks | Docker and GitHub Actions | Planned |

Technology choices remain subject to the comparison of alternatives and experimental validation. No target metric should be interpreted as an achieved result.

## Documentation and repository organisation

The following paths describe the prepared local package and intended repository structure. Apart from this README, these materials have not yet been uploaded; paths below are not download links.

| Path | Content |
| --- | --- |
| `docs/report.html` | Editable draft covering proposal, relevance, literature, system and technology comparisons, requirements, architecture, prototype, evaluation, management and supervisor feedback |
| `docs/sources.json` | Draft source catalogue for verification and critical review |
| `docs/requirements.json` | Initial requirements and acceptance criteria; owner assignments need reconciliation |
| `docs/survey-questions.txt` | English survey questions |
| `diagrams/` | Context, use-case and component diagrams, with Mermaid source and SVG exports |
| `prototype/index.html` | Interactive UI mock-up |
| `tests/` | Manual prototype checklist and package-structure checks |
| `management/` | Draft task plan and templates for recording genuine discussion and supervisor-review evidence |
| `config/` | Configuration examples and project-link placeholders |
| `src/` | Implementation status; production implementation pending |

Before submission, the literature review must meaningfully use at least 12 sources, including 8 scientific publications. Comparisons must cover 3–5 existing systems using 6–10 criteria and at least three technical decisions with 2–3 alternatives each. The final report must distinguish evidence from assumptions.

## Project links

- Repository: https://github.com/6wq22pbr26-droid/phishlens-diploma
- English research survey: https://docs.google.com/forms/d/e/1FAIpQLSeKItS51CarKIaIW3Mt9TAiw5Keploe_ShI60XnwVSWySVP2g/viewform
- YouTrack project and board: **pending team setup; link will be added after confirmation**.
- Reviewed documentation and prototype links: **pending upload**.

The survey is a research instrument, not the university submission form. Survey responses alone do not automatically replace the required 3–5 user discussions or a substantive agreement with an actual client.

## Setup and verification

There is no installable extension or runnable backend in this repository yet.

After the prototype package is uploaded, open `prototype/index.html` in a browser. It is a UI mock-up with manually selected states; it does not analyse real websites or provide phishing protection. No server or dependencies are required for the mock-up.

After the supporting files are uploaded:

- Follow `tests/manual-checklist.txt` to check the prototype scenarios.
- Run `python3 tests/check_package.py` from the repository root for a package-structure check.

A structure check does not validate the literature, research evidence, model accuracy or extension behaviour. Reproducible installation and test commands for implemented components will be added when those components exist.

## Contribution and review workflow

1. Create a meaningful YouTrack task with an assignee, priority, deadline, expected result and acceptance criteria.
2. Use the actual YouTrack task ID in the branch name, commit message and Pull Request description.
3. Each contributor works through their own identifiable GitHub account and records coherent changes as work is completed.
4. Open a Pull Request explaining the change, task reference and verification performed.
5. Another team member reviews the change before it is merged into `main`.
6. Link the Pull Request or commit from YouTrack. Mark the task complete only after its acceptance criteria are met.
7. Tag the reviewed submission version using the stage tag required by the school; do not move a tag after submission.

The initial repository setup is not evidence of completed individual work. Do not backdate contributions or record unperformed research, tests or reviews.

## Checkpoint and access

Submission deadline: **24 October 2026, 18:00, Asia/Almaty**.

Remaining checkpoint work includes reviewing and uploading the draft materials, adding genuine research findings, obtaining and addressing supervisor feedback, completing the YouTrack board, and documenting individual contributions and reviews.

The submission requires a consolidated report PDF and a separate PDF containing screenshots of the real YouTrack board and tasks. The private repository and linked materials must be accessible to the supervisor and committee before submission. Their access has not yet been verified.

## Data handling and limitations

Do not commit passwords, API keys, private credentials, identifiable survey responses or interview transcripts. Use anonymised summaries and placeholder configuration values. Assess dataset licences, attribution requirements, duplicate records and train/test leakage before using data. Model export, local inference and external reputation services must be evaluated before their capabilities are claimed.
