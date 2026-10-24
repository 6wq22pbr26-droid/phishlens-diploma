# PhishLens

**Design and Development of an Explainable Browser Extension for Real-Time Phishing Website Detection**

Software Engineering · SE-2422 · Supervisor: A. A. Sakhipov, PhD, Assistant Professor.

## Read the project

| Material | Open in GitHub |
| --- | --- |
| Final report — all 11 sections and evidence | [Read the report page by page](docs/REPORT.md) |
| Original final PDF | [SE-2422 Pangerey ProbPeriod1](docs/SE-2422_Pangerey_ProbPeriod1.pdf) |
| Requirements and MVP scope | [Read requirements](docs/01_Requirements_and_MVP_Scope.md) |
| Supervisor feedback | [Read the feedback table](docs/02_Supervisor_Feedback_Record.md) |
| Team response | [Read the changes](docs/03_Team_Response_and_Change_Record.md) |
| Architecture and editable diagrams | [View diagrams](diagrams/README.md) |
| Interactive interface mock-up | [Prototype and opening instructions](prototype/README.md) |
| Task plan and YouTrack evidence | [Project management](management/README.md) |
| Evaluation and checks | [Evaluation materials](tests/README.md) |

## Project status

The project is at the analysis and design stage. The package includes a 12-response student survey, literature review, comparisons, requirements, architecture, interface mock-up, evaluation plan and a 19-task schedule. The extension, supporting API and trained model are planned work. F1 >= 0.90 and local latency <= 200 ms are evaluation targets.

The first MVP covers URL checking, a baseline model, local inference where feasible, a popup with risk and reasons, and a minimal FastAPI contract. Later work includes richer features, explanations, optional reputation checks, caching, settings and localization.

## Team

| Member | GitHub | Planned responsibility |
| --- | --- | --- |
| Aiym Pangerey | [aiympangerey1703](https://github.com/aiympangerey1703) | Coordination; shared frontend/backend; architecture and integration |
| Sabina Zhumagaliyeva | [6wq22pbr26-droid](https://github.com/6wq22pbr26-droid) | Shared frontend/backend; interface, settings and testing |
| Alibek Asylbekuly | [alibek44](https://github.com/alibek44) | Machine learning, evaluation and model packaging |

## Evidence and next steps

The questionnaire is preliminary evidence from 12 respondents; Q7 has 11 answers. Q12 contains inconsistent exclusive-option selections and needs review of individual records. User discussions and prototype usability testing remain planned. Model training, extension/API implementation, performance evaluation and substantive peer reviews are subsequent work.

The supervisor gave positive overall feedback on the presented materials and requested a consolidated PDF. The feedback table records this without assigning unrecorded detailed comments to the supervisor. No private correspondence image is included in the current files.

## Versions and access

The supplied PDF is preserved byte for byte. It cites the original `prob-period-1` baseline at `c5a2aeb96f6c9096a3a5c9cc8bcd24a9098d9807`. This readable publication update is separate from that historical baseline. [Version notes](docs/VERSION_NOTES.md) explain the distinction.

The repository is private. Reviewers need access to this repository and the [YouTrack instance](https://aiympangerey1703.youtrack.cloud). Word and ZIP files are downloads; the Markdown pages and images above provide browser-readable copies.
