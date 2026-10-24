# Requirements and MVP scope

PHD-1 | Version 0.1 | Submission copy: 24 October 2026

Design and Development of an Explainable Browser Extension for Real-Time Phishing Website Detection

We propose a browser extension that checks a visited website for phishing indicators and explains the risk in plain language. This document defines the first working version and the criteria the team will use to assess it. Implementation has not started; the scope and targets below require team and supervisor review.

## Users and first working version

The primary users are everyday internet users, including students and staff. The first version will target a Chromium browser using Manifest V3. Support for other browsers can follow after the initial workflow works reliably.

The MVP covers page URL checking, a baseline ML model, local inference where feasible, a popup with the risk and reasons, and a minimal backend API. Later stages add DOM and domain signals, reputation integrations and caching, localization, feedback storage, and broader testing.

## Functional requirements

| ID | Requirement and acceptance condition |
| --- | --- |
| FR-01 | Check the active page URL on supported navigation events. Ignore internal browser pages and handle missing or invalid URLs without crashing. |
| FR-02 | Apply a reproducible feature pipeline and baseline model. Return a documented risk result; show unavailable or uncertain results explicitly. |
| FR-03 | Display the result in the popup with understandable reasons linked to observable indicators. Present the result as a risk assessment, with limitations. |
| FR-04 | Define the extension and ML input/output contract. Provide a FastAPI service with validated schemas, documented responses, and clear failure handling. |
| FR-05 | Keep browsing history off the server. Document any individual URL or domain sent for a selected reputation check and review this data flow before enabling it. |
| FR-06 | Make the extension installable in developer mode from the repository. Document installation, startup, a safe demonstration, and known limitations. |


## Deferred scope

Planned after the baseline MVP: richer DOM/domain features; model explanations and browser packaging; reputation sources; Redis caching; user feedback and permitted result storage; kk/ru/en localization; Docker; continuous integration; functional, load, and usability evaluation. These remain part of the diploma plan, but do not all block the first prototype.

## Privacy and technical constraints

Local processing is the preferred design for page analysis. Page content, form entries, passwords, cookies, and browsing history must not be uploaded by default. Backend, external reputation lookups, feedback collection, and any stored results need an explicit data-flow description. Store only justified fields; document retention and deletion before implementing storage.

| ID | Target and how it will be assessed |
| --- | --- |
| NFR-01 | Detection quality: proposed F1 target of at least 0.90 on held-out data. Report precision, recall, F1, ROC-AUC, class balance, and errors. Split and deduplicate data to reduce leakage; do not tune on the final test set. |
| NFR-02 | Latency: proposed local feature extraction plus inference target of at most 200 ms. Record browser, hardware, model, and measurement method. Measure external lookup/API latency separately and discuss the end-to-end result. |
| NFR-03 | Reliability and usability: show loading, unavailable, timeout, and error states. Test safe examples without requiring users to open live phishing sites. Evaluate multilingual text and usability in the later system evaluation. |


## Responsibilities and schedule

| Member | Responsibilities |
| --- | --- |
| Aiym | Team lead; shares frontend/backend development with Sabina; architecture, URL checking, API, and integration coordination. |
| Sabina | Shares frontend/backend development with Aiym; popup and warnings, settings, localization, storage, and system/usability testing. |
| Alibek | Dataset preparation, feature extraction, model training and evaluation, explanations, and model packaging. The whole team verifies integration. |


PHD-1 is due 26 October 2026. Research and architecture are planned for November; the baseline prototype for January 2027; explanations and integration for February–March; system testing by 23 April. The overall project period supplied by the supervisor ends on 10 May 2027. Individual task dates are team planning dates.

## Review record — 24 October 2026

The supervisor gave a general positive response to the supplied materials and requested a consolidated PDF report. The response did not provide detailed technical validation of the targets. This copy preserves the agreed planning scope and PHD-1 deadline of 26 October 2026. The university submission deadline remains 24 October 2026 at 18:00 (Asia/Almaty).
