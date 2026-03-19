# QA Findings Report
## Quality Assurance Audit — Requirements Engineering Process
### Biometric Student Attendance System

---

**Document ID:** PA-QAR-2026-001
**Version:** 1.0
**Date:** 18 March 2026
**Audit Period:** 15–18 March 2026
**Prepared by:** Paragon Assurance
**Submitted to:** BioSec Educational Institution (Customer C)

| Name | Role |
|---|---|
| Zong Han | QA Auditor |

---

## Executive Summary

Paragon Assurance conducted an independent Quality Assurance (QA) audit
of the Requirements Engineering (RE) process carried out by Nevon
Solutions for BioSec Educational Institution under Project P2-1561W,
covering the Biometric Student Attendance System. The audit evaluated
adherence to process obligations and documentation standards across the
Analysing, Specifying, and Validating phases. The review is bounded to
process compliance; the correctness of individual requirement statements
falls outside the audit scope. This report additionally addresses the
process completeness of the QC audit commissioned to inspect the SRS.

Overall, the RE process is assessed as **substantially compliant**. The
Analysing phase demonstrates complete BCIC execution: the IRC functioned
as a standalone controlled document, requirements carry a consistent
identifier scheme (BOR/TR), and models are traceable from their original
PS versions to revised AR versions. The Specifying phase is fully
evidenced: the SRS cites a recognised template, all repository
requirements are present in the SRS, the iRTM is available as a
standalone extractable file, and a change management template exists in
the repository. The Validating phase yields one resolved non-conformance
(QA-V-01: BioSec customer sign-off confirmed by NS-DECL-2026-001
committed to the repository) and one open item (QA-V-02: no documentary
evidence of editorial checks was found). The QC team process remains
unconfirmed: no QC plan, checklist, or findings report was located in
the repository or in any artefact supplied to this audit.

---

## 1. QA Audit

### 1.1 Execution Plan

#### Context and Goals

BioSec Educational Institution C-staff commissioned Paragon Assurance
to perform an independent QA audit of the requirements engineering
process carried out by Nevon Solutions in connection with the
authentication of the SRS. All artefacts were supplied by Nevon
Solutions and reviewed remotely under a desktop review model.
Confidentiality of all supplied materials is observed throughout the
engagement.

**The goals of this audit are:**

- To assess whether the Analysing, Specifying, and Validating phases
  were each planned, executed, and closed with the required artefacts
  and documentation.
- To record and report instances where process obligations were not met
  or supporting documentation was absent.
- To verify the process completeness of the QC audit by establishing
  whether the assigned QC team produced a documented plan, a checklist,
  and recorded findings.

#### Work Breakdown

| Phase | Activities | Assignee |
|---|---|---|
| Phase 1: Preparation | Identify required artefacts; confirm repository access; prepare audit checklist (PA-QA-2026-002-CL) | Zong Han |
| Phase 2: Evidence Collection | Access and collect all artefacts from Nevon Solutions project repository | Zong Han |
| Phase 3: Process Verification | Apply each checklist item against available artefacts; request supplementary evidence where needed | Zong Han |
| Phase 4: Observation Recording | Record all unconfirmed checklist items as process non-compliance findings with evidence references | Zong Han |
| Phase 5: Reporting | Compile findings by stage; consolidate overall QA process assessment; finalise report | Zong Han |

**Phase 1: Preparation**

Required artefacts for this audit were identified as the Analysing
Report (NS-AR-2026-001), the Software Requirements Specification
(NS-SRS-2026-001), the Project Specification (BS-PS-2026-001), the
Incongruous Requirements Checklist (NS-IRC-2026-001), the iRTM, the
Gantt Chart, the Change Request Form Template, the IEEE SRS template,
and the requirements model files. Repository access was confirmed. The
audit checklist (PA-QA-2026-002-CL) covering the Pre-Audit setup,
Analysing, Specifying, and Validating phases was prepared prior to
commencement of the review (see Section 1.2 for the completed checklist).

**Phase 2: Evidence Collection**

All artefacts were accessed from the Nevon Solutions project repository.
The following were collected and reviewed for checklist application:
Analysing Report (NS-AR-2026-001), Software Requirements Specification
(NS-SRS-2026-001), Project Specification (BS-PS-2026-001), Incongruous
Requirements Checklist (NS-IRC-2026-001), iRTM (standalone .docx), Gantt
Chart, Change Request Form Template, IEEE SRS template,
bizops-requirements.md, technical-requirements.md, context-diagram.pdf,
and paper-napkin-model.jpg. All files confirmed present in the repository.

**Phase 3: Process Verification**

Each checklist item was applied against the available artefacts to
establish whether the expected RE activities had been carried out and
documented. Where direct inspection of the artefacts was insufficient
to reach a conclusion, supplementary evidence was requested from Nevon
Solutions. All checklist items were evaluated against the complete body
of evidence, encompassing both repository artefacts and any additional
records supplied by the vendor.

**Phase 4: Observation Recording**

Any checklist item that could not be confirmed from available evidence
was recorded as a process non-compliance finding. Each finding includes
an issue characteristic, an observation drawn from the specific
artefact under review, the follow-up action taken, and the resulting
conclusion. All findings are grounded exclusively in direct inspection
of the supplied artefacts and repository; no assumptions were made
beyond what the evidence directly supports.

**Phase 5: Reporting**

All non-compliance instances were compiled by stage and presented in
Section 1.3 with supporting evidence references. Section 1.4
consolidates the overall QA process assessment. This report was updated
on 18 March 2026 to incorporate the vendor-submitted BioSec Change
Request Declaration Form (NS-DECL-2026-001) and revise findings
accordingly.

#### Checklist Application

A purpose-built audit checklist was used to evaluate whether the RE
process activities were performed and documented at each phase. Section
1.2 presents the completed checklist with the status and evidence
recorded for each item. Each entry carries a Checklist ID, item
description, applicable investigation method, Status, Evidence
Location, and Notes, covering Pre-Audit setup, the Analysing,
Specifying, and Validating phases, and QC process checks.

Checklist items where process non-compliance was identified are
escalated to Section 1.3 as formal findings. Each finding is structured
with a Task ID and Description, Issue Characteristic, Observation,
Follow-Up Action and Result, and Evidence.

---

### 1.2 RE Process Checklist

Three investigation methods were applied across checklist items:

**Method 1 — Artefact Inspection:** Direct examination of files and
documents in the repository to confirm existence, format, and
completeness.

**Method 2 — Traceability & Cross-Reference:** Comparing requirements or
items across multiple documents to verify consistency and chain of
custody.

**Method 3 — Declaration & Sign-Off Review:** Verifying formal approvals,
signed declarations, interview records, and process self-checks.

**Rating key:** Pass | Partial | Missing | Pending | N/A

| ID | Checklist Item | Method | Status | Evidence Location | Notes |
|:---|:---|:---|:---|:---|:---|
| P1 | Have you scheduled an interview/focus group with the customer? | M3 | Pending | Annex 6 (reserved) | Interview required to close QA-V-02; not yet conducted |
| P2 | Do you have access to the customer's repository? | M1 | Pass | GitHub repository | Confirmed read access |
| A1 | Does the customer have a copy of the Project Scope (PS)? | M1 | Pass | Project Specification\_1561W.pdf | Present in repository |
| A2 | Have the models from the PS been carried forward into the Analysis phase? | M1 | Pass | paper-napkin-model.jpg; context-diagram.pdf | Both models present in AR |
| A3 | Is there proof that the models were revised? | M1 | Pass | context-diagram.pdf; AR Appendix B | Revised version in AR; original retained in PS |
| A4 | Does the IRC exist? | M1 | Pass | IRC\_Nevon\_Solutions.pdf | Standalone document confirmed |
| A5 | Is the IRC usable? | M1 | Pass | IRC\_Nevon\_Solutions.pdf | Checklist format; 9 categories; extractable as standalone |
| A6 | Is there evidence the IRC was used? | M1 | Pass | IRC\_Nevon\_Solutions.pdf | 9 categories completed with project-specific findings |
| A7 | Did the customer have a written plan for the Analysis phase? | M1 | Pass | BioSec Gantt Chart.xlsx | Structured sessions BC-01 and TC-02 assigned |
| A8 | If the plan was verbal only, did they provide a signed declaration? | M1 | N/A | BioSec Gantt Chart.xlsx | Plan was documented; verbal-only declaration not required |
| A9 | Were items from the PS properly codified in the repo? | M1 | Pass | bizops-requirements.md; technical-requirements.md; iRTM.docx | BOR/TR identifier scheme applied |
| B1 | Do the requirements in the SRS trace back to the repo? | M1, M2 | Pass | SRS\_1561W.pdf §§4–6; iRTM.docx | All repo requirements traced to SRS; chain of custody confirmed |
| B2 | Does the iRTM exist as a standalone file? | M1, M2 | Pass | iRTM.docx | Standalone .docx file; not embedded in PDF |
| B3 | Is the iRTM usable? | M1, M2 | Pass | iRTM.docx | Single extractable unit |
| B4 | If new models were created in this phase, are the source files present? | M1 | N/A | Repository inspection | No new models created in the Specifying phase |
| B5 | If a Change Mitigation template is mentioned, does the template file exist? | M1 | Pass | Change Request Form Template.docx | Template present in repository |
| C1 | Is the SRS signed off by the customer? | M2, M3 | Pass | BioSec\_Change\_Request\_Form.docx (NS-DECL-2026-001); Annex 5 | Resolved via QA-V-01 follow-up; committed to repository |
| C2 | Is there evidence of a spell check? | M3 | Partial | SRS\_1561W.pdf Declaration page | No documentary evidence found; QA-V-02 open |
| C3 | Is there evidence of a grammar check? | M3 | Partial | SRS\_1561W.pdf Declaration page | No documentary evidence found; QA-V-02 open |
| C4 | Is there evidence of an editorial check? | M3 | Partial | SRS\_1561W.pdf Declaration page | No documentary evidence found; QA-V-02 open |
| D1 | Does the QC team have a written plan for their review? | M3 | Missing | Repository inspection | No QC plan located in repository or artefacts supplied |
| D2 | Does the QC team have a checklist (similar to an IRC)? | M3 | Missing | Repository inspection | No QC checklist located |
| D3 | Did the QC team check for Scenario errors? | M3 | Missing | Repository inspection | No QC findings report located |
| D4 | Did the QC team check for Persona errors? | M3 | Missing | Repository inspection | No QC findings report located |
| D5 | Did the QC team check for Assumption errors? | M3 | Missing | Repository inspection | No QC findings report located |
| D6 | Did the QC team save their findings? | M3 | Missing | Repository inspection | No QC findings report located |
| F1 | Did you have to ask for any declarations? | M3 | Pass | NS-DECL-2026-001; Annex 5 | Declaration requested and obtained; placed in Annex 5 |
| F2 | Did you use interviews or focus groups? | M3 | Pending | Annex 6 (reserved) | Interview/focus group pending for QA-V-02 |
| F3 | In your presentation/findings, did you avoid suggesting solutions? | M3 | Pass | Report text | Self-check: no corrective actions prescribed in findings |

---

### 1.3 Error Detection

The non-compliance instances identified during the Nevon Solutions RE
process audit are recorded in this section. All findings originate from
direct inspection of the AR, SRS, and project repository. The
non-compliance instances encountered fall under the following issue
characteristics:

- **Undocumented activity:** An activity is referenced or implied in the
  artefact, but no supporting record was produced or located to
  independently confirm that it took place.
- **Required deliverable missing:** A deliverable required at the
  conclusion of a phase was not produced, or is absent from all
  artefacts and repository locations reviewed.

#### 1.3.1 Analysing Stage

No process non-conformances were identified in the Analysing phase. All
nine checklist items (A1 to A9) were confirmed as passing based on
documentary evidence in the repository. See Section 1.2 for full
checklist results.

#### 1.3.2 Specifying Stage

No process non-conformances were identified in the Specifying phase. All
applicable Specifying checklist items (B1 to B5) were confirmed as
passing or not applicable based on documentary evidence in the
repository. See Section 1.2 for full checklist results.

#### 1.3.3 Validating Stage

| **Task ID: QA-V-01 — Requirements Change Documentation** | **Issue Characteristic: Required deliverable missing** |
|:---|:---|

**Observation:**
During a traceability review of the PS, AR, and SRS, two categories of
undocumented changes were identified. First, five institutional policy
values were embedded in the SRS with no documented source in the PS or
AR: the attendance calculation tolerance (±5 minutes), late arrival
threshold (>15 minutes after class start), absence threshold (>50% of
attendance period missed), leave approval SLA (24 hours), and medical
certificate requirement (>3 consecutive days absent). These represent
BioSec policy decisions requiring formal customer sign-off. Second,
three open issues from AR Section 3.5, acknowledged in SRS Section 8.2
with a kill date of 15/03/2026, had no recorded resolution sign-off
(CM-OI-01, CM-OI-02, CM-OI-03). At the time of initial review, the
completed Change Request Form had not been committed to the repository.

**Follow-Up Action and Result:**
Paragon Assurance identified the undocumented changes and notified
Nevon Solutions. The BioSec Change Request Declaration Form
(NS-DECL-2026-001, dated 24 February 2026) was subsequently committed
to the project repository. All five Section A thresholds and three
Section B open issue resolutions were confirmed (Y) by BioSec. This
item is resolved.

**Evidence:**
BioSec\_Change\_Request\_Form.docx (NS-DECL-2026-001, Annex 5);
SRS\_1561W.pdf Sections 4–6 (threshold values);
Analysing Report\_1561W.pdf Section 3.5 and SRS Section 8.2 (open issue references).

---

| **Task ID: QA-V-02 — Editorial Checks on SRS** | **Issue Characteristic: Undocumented activity** |
|:---|:---|

**Observation:**
No documentary evidence of spell check, grammar check, or editorial
review completion was found in the repository or in any artefacts
reviewed. The SRS Declaration page states the document was *"reviewed,
validated, and approved"* by the Project Lead, but does not record
editorial checks as a distinct activity. No checklist, annotation, or
signed record confirming these activities was located in the repository.

**Follow-Up Action and Result:**
This item requires confirmation via interview or focus group with Nevon
Solutions to establish whether spell, grammar, and editorial checks were
performed prior to SRS submission. No follow-up confirmation has been
received at the time of this report. Annex 6 is reserved for the
interview or focus group record when obtained.

**Evidence:**
SRS\_1561W.pdf Declaration page; full repository inspection (no editorial check record found).

---

### 1.4 Final Findings

The Analysing and Specifying phases of the Nevon Solutions RE process
for Project P2-1561W are complete and well-evidenced. All Analysing
phase items (A1 to A9) and all applicable Specifying phase items (B1 to
B5) were confirmed as passing or not applicable based on documentary
evidence in the repository. Key strengths include the thorough and
systematic use of the IRC (NS-IRC-2026-001), clear traceability of
models from original to revised versions, and the presence of all
required standalone artefacts (IRC, iRTM, Change Request Form Template,
IEEE SRS template).

QA-V-01 (Requirements Change Documentation) is compliant. The BioSec
Change Request Declaration Form (NS-DECL-2026-001) has been committed to
the repository, confirming all five quantitative thresholds (Section A)
and three open issue resolutions (Section B). This item is resolved.

QA-V-02 (Editorial Checks) is partially compliant. The SRS Declaration
page confirms the document was reviewed and approved by the Project Lead,
but no documentary evidence of distinct editorial check activities was
found in the repository. This item requires follow-up interview or focus
group with Nevon Solutions to determine its final status.

*(QC audit findings — see Section 2.)*

---

## 2. QC Audit

### 2.1 Execution Plan

*(To be completed.)*

### 2.2 QC Checklist

| ID | Checklist Item | Status | Evidence Location | Notes |
|:---|:---|:---|:---|:---|
| D1 | Does the QC team have a written plan for their review? | | | |
| D2 | Does the QC team have a checklist? | | | |
| D3 | Did the QC team check for Scenario errors? | | | |
| D4 | Did the QC team check for Persona errors? | | | |
| D5 | Did the QC team check for Assumption errors? | | | |
| D6 | Did the QC team save their findings? | | | |

### 2.3 Error Detection

*(To be completed.)*

### 2.4 Final Findings

*(To be completed.)*

---

## Sign Off

Upon completion of the desktop QA audit of the Nevon Solutions RE
process, this report is formally submitted to BioSec Educational
Institution C-staff. Sections 1.3 and 1.4 constitute the complete
record of process non-compliance identified by Paragon Assurance during
this engagement. This report documents findings only; no corrective
actions or remediation steps are prescribed.

---

| Role | Name | Signature | Date |
|---|---|---|---|
| QA Auditor | Zong Han | ________________ | 18/03/2026 |

---

\newpage

## Annexes

*Annexes contain physical copies of standalone external artefacts
referenced as evidence in this report. To be populated as evidence is
gathered, particularly for items requiring follow-up (QA-V-02).*

| Annex | Description |
|---|---|
| Annex 1 | IRC — Incongruous Requirements Checklist (NS-IRC-2026-001) — evidence for A4, A5, A6 |
| Annex 2 | Analysing Report cover page and sign-off — evidence for A1, A7 |
| Annex 3 | SRS Section 1.2 (template reference) — evidence for B1 |
| Annex 4 | SRS Section 1.1 and iRTM reference — evidence for B1, B2 |
| Annex 5 | BioSec Change Request Declaration Form (NS-DECL-2026-001) — evidence for QA-V-01 |
| Annex 6 | *(To be added)* Interview/focus group record — pending QA-V-02 follow-up |

---

## Appendix A — Glossary

| Term | Definition |
|---|---|
| QA | Quality Assurance. The process of auditing the RE process for compliance with defined process requirements. QA audits the *process*, not the work product. |
| QC | Quality Control. The process of inspecting a work product (e.g., the SRS) for authorship defects, omissions, and contradictions. QC audits the *product*, not the process. |
| RE | Requirements Engineering. The structured set of methods used to elicit, analyse, document, and validate software requirements, comprising the Analysing and Specifying methods. |
| Analysing Method | The RE method comprising Breakdown and Clarify phases, applied to the customer's Project Specification to produce a regulated-revision requirements repository ready for Specifying. |
| Specifying Method | The RE method comprising Interpret, Categorise, and Specify phases, applied to the requirements repository to produce the Software Requirements Specification (SRS). |
| BCIC | Breakdown, Clarify, Interpret, Categorise. The four core activities of the RE Analysing method. |
| Process Non-Compliance | The sole error type for QA audits. An instance where the RE process deviated from defined process requirements, either through omission, incorrect execution, or unauthorised deviation. |
| CRaM | Crisp, Realistic and Measurable. The quality criterion applied to requirements and findings to ensure they are clear, grounded in evidence, and quantifiable where applicable. |
| SRS | Software Requirements Specification. The primary work product of the Specifying method, serving as the contractual requirements baseline between customer and vendor. |
| IRC | Incongruous Requirements Checklist. The tool used during the Breakdown phase to assess each PS requirement for ambiguity, incompleteness, non-testability, technical infeasibility, and compound structure. |
| iRTM | Inceptive Requirements Traceability Matrix. The traceability artefact that establishes chain-of-custody from the Project Specification through to the SRS. |
| Open Issue | A specification matter that was identified during the Analysing phase but could not be resolved during clarification sessions, documented with a stated deadline and responsible party for resolution before SRS finalisation. |
| PDPA | Personal Data Protection Act (Singapore, 2012, as amended). The legislative framework governing the collection, use, storage, and disposal of personal data, applicable to all biometric and attendance data in this project. |
| AR | Analysing Report. The document produced by the vendor team following BCIC-based regulated revision of the Project Specification. |
| PS | Project Specification. The customer's source document for requirements. |

---

*End of PA-QAR-2026-001*
