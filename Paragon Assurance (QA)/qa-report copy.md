# PARAGON ASSURANCE
## Quality Assurance Audit Report
### Requirements Engineering Process — Biometric Student Attendance System

---

**Document ID:** PA-QAR-2026-001
**Version:** 1.0
**Date:** 19 March 2026
**Prepared by:** Paragon Assurance QA Audit Team
**Submitted to:** BioSec Educational Institution (Customer C)

| Name | Role |
|---|---|
| [QA Audit Lead Name] | QA Audit Lead |
| [QA Auditor 1 Name] | QA Auditor |
| [QA Auditor 2 Name] | QA Auditor |
| [QA Auditor 3 Name] | QA Auditor |

---

## Table of Contents

1. Executive Summary
2. QA Plan
3. QA Checklist
4. QA Error Detection
5. QA Findings
6. Sign-Off
7. Addenda

   - Annex A — QA Work Allocation and Timeline
   - Glossary

---

---

## 1. Executive Summary

### 1.1 Audit Context

Paragon Assurance was engaged by BioSec Educational Institution as an independent external Quality Assurance (QA) vendor to audit the Requirements Engineering (RE) process conducted by Nevon Solutions for the Biometric Student Attendance System. The RE process under audit encompasses the Analysing method (Breakdown and Clarify phases) and the Specifying method (Interpret, Categorise, Specify phases, culminating in the production of the Software Requirements Specification).

The principal process artefacts reviewed are:

- Analysing Report, Document ID: NS-AR-2026-001, Version 1.0, dated 08 February 2026
- Software Requirements Specification (SRS), Document ID: NS-SRS-2026-001, Version 0.8, dated 03 March 2026
- QC Audit Report, Veridion Labs (QC), as provided to the QA team
- Requirements repository artefacts (GitHub: https://github.com/wenxuannx/Biometric-Student-Attendance-System)
- Clarification session minutes: BC-01 (07/02/2026) and TC-02 (09/02/2026)

### 1.2 Audit Goals

The QA audit was conducted to establish the degree of compliance of Nevon Solutions' RE process with the process requirements applicable to the Analysing and Specifying methods, and to identify any instances of process non-compliance that may affect the completeness, correctness, or authorisation status of the deliverables presented to BioSec.

### 1.3 Summary of Findings

The audit identified **seven (7) process non-compliance instances**. Two (2) are classified as High severity, three (3) as High-to-Medium severity, one (1) as Medium severity, and one (1) as Low severity. Key non-compliance areas are:

- Three open issues from the Analysing phase remain unresolved in the submitted SRS despite a stated resolution deadline of 20 February 2026.
- The SRS sign-off section (§9) was submitted to external audit with all four designated approver fields blank, indicating the SRS was not formally authorised by BioSec before handover.
- A contradictory 2FA scope specification was not resolved during the Clarify phase.
- The biometric student enrolment process — a prerequisite for all scan-based system functions — was not elicited during the Analysing phase and is entirely absent from the SRS.
- A cross-section attendance status terminology inconsistency was not detected or corrected during the Specifying phase.
- The SRS was submitted at Version 0.8, below the Version 1.0 threshold expected for a document released to external audit.
- A grammatical defect in requirement QA-USAB-01 was not corrected by the Specifying phase editorial review.

The QA team presents these findings without amendment to BioSec for review and decision.

---

---

## 2. QA Plan

### 2.1 Target Process Description

The process under audit is the Requirements Engineering (RE) process as performed by Nevon Solutions for the Biometric Student Attendance System project, Customer BioSec Educational Institution, Project Reference P2-1561W.

The RE process under audit comprises two sequential methods:

**Analysing Method** — the structured process for receiving the BioSec Project Specification (BS-PS-2026-001, Version 1.0), assessing all requirements for congruency using the Incongruous Requirements Checklist (IRC), resolving incongruities through facilitated stakeholder clarification sessions, and producing a regulated-revision repository of requirements ready for Specifying.

Specific phases audited:
- Breakdown phase: IRC application, incongruity categorisation, compound decomposition
- Clarify phase: Stakeholder engagement (BC-01 and TC-02 sessions), resolution documentation, open issue management

**Specifying Method** — the structured process for interpreting, categorising, and specifying the analysed requirements into the SRS document (NS-SRS-2026-001), including traceability, quality assurance of individual requirement statements, production of supporting artefacts, and SRS authorisation.

Specific phases audited:
- Interpret and Categorise phases: requirement translation and classification
- Specify phase: SRS drafting, cross-section consistency, editorial quality review
- Finalisation: version control, open issue resolution, SRS sign-off

### 2.2 Audit Context and Goals

**Context:** The BioSec project involves the development of a cloud-hosted Biometric Student Attendance Management System to replace a manual paper-based process across five campuses in Singapore. The system handles biometric fingerprint data from minors and must comply with Singapore's Personal Data Protection Act (PDPA). The sensitivity of the data and the regulatory obligations make process compliance in the RE phase critical to downstream quality.

The QA team was provided access to: the Analysing Report (including BC-01 and TC-02 session minutes), the SRS, the requirements repository, the QC Audit Report from Veridion Labs, and the project repository. The QA team also sought information from the QC team (Veridion Labs) as a supplementary evidence source.

**Goals:**
1. Determine whether the Analysing method was applied in full, including complete IRC assessment, effective stakeholder clarification, and proper open issue management.
2. Determine whether the Specifying method produced an SRS that complies with process requirements for completeness, consistency, traceability, and formal authorisation.
3. Identify all instances of process non-compliance with evidence sufficient for customer review and decision.

### 2.3 Work Breakdown

See Annex A for the detailed team work allocation and indicative audit timeline.

The audit was structured in four phases:

| Phase | Activities | Assignee(s) |
|---|---|---|
| Phase 1: Document Review | Review of all process artefacts; Analysing Report, SRS, QC report, repository | All team members |
| Phase 2: Checklist Assessment | Completion of QA Checklist against each process phase | QA Auditors |
| Phase 3: Error Detection & Evidence | Identification and documentation of non-compliance instances | QA Auditors |
| Phase 4: Finding Analysis & Sign-off | CRaM analysis, evidence consolidation, report finalisation | QA Audit Lead |

---

---

## 3. QA Checklist

The following checklist is self-contained and addresses process compliance across three domains: the Analysing method, the Specifying method, and process artefact integrity. Each item is assessed against the evidence available from the process documentation.

**Rating key:** S = Satisfied | PS = Partially Satisfied | NS = Not Satisfied | N/A = Not Applicable

---

### Domain A — Analysing Method Compliance

| ID | Checklist Item | Rating | Notes |
|---|---|---|---|
| A.1 | Were all PS requirements subjected to the Breakdown/IRC analysis (congruency check)? | S | Analysing Report §2.1–2.2 documents full IRC application across all 27 PS requirements. Five incongruity categories assessed. |
| A.2 | Were all ambiguous requirements quantified during the Clarify phase? | PS | Most ambiguous requirements were resolved (BC-01 outcomes, §3.3). BOR-1-MOB-01 still references "institutional policies" without specific policy documents (noted as flagged; resolution pending). |
| A.3 | Were clarification sessions conducted with all relevant stakeholder groups? | S | BC-01 (07/02/2026) included BioSec Academic Administrator, Parent Representative, Campus Operations Manager, Account Manager. TC-02 (09/02/2026) included BioSec IT Manager, Network Infrastructure Lead. Both sessions are documented in §3.3 and §3.4 of Analysing Report. |
| A.4 | Were meeting minutes formally recorded with attendees, focus, and outcomes documented? | S | Both BC-01 and TC-02 are documented in Analysing Report §3.3 and §3.4 with attendees, clarification focus, and key outcomes. |
| A.5 | Were all compound requirements decomposed into atomic requirements? | S | Analysing Report §2.2–2.3 documents decomposition of BOR-1-MOB-02, BOR-1-MOB-03, BOR-1-WEB-01, BOR-1-WEB-02, TR-1-BE-01, and TR-1-BE-05 into atomic requirements with traceability. |
| A.6 | Were open issues formally documented with resolution deadlines? | PS | Analysing Report §3.5 documents three open issues with stated deadlines and assigned parties. However, the RPO/RTO deadline of 20/02/2026 was not met prior to SRS finalisation (see Error PA-ERR-001). |
| A.7 | Was the biometric enrolment process elicited as part of the Analysing phase? | NS | No enrolment requirement appears in either the repository or the SRS. BC-01 and TC-02 outcomes make no reference to enrolment. See Error PA-ERR-004. |

---

### Domain B — Specifying Method Compliance

| ID | Checklist Item | Rating | Notes |
|---|---|---|---|
| B.1 | Are all SRS requirements traceable to PS/repository requirements via iRTM (Appendix D)? | PS | iRTM is present in SRS Appendix D. However, the absence of enrolment requirements (PA-ERR-004) means the iRTM cannot account for this process gap. |
| B.2 | Do SRS requirement statements meet CRaM criteria (atomic, unambiguous, testable)? | PS | Most requirements meet CRaM. QA-USAB-01 contains a double-verb grammatical defect (PA-ERR-007). "Periodic synchronisation" in §2.3 is vague relative to the quantified 5-minute sync in FR-COM-01 (confirmed by QC-FND-008). |
| B.3 | Is terminology consistent across all SRS sections and artefacts? | NS | Attendance status terminology is inconsistent: UR-MOB-01 uses "Attended, Absent, Late, or Excused"; §4.3.2 Stimulus/Response uses "Excused, Attended, Late, Absent." QC-FND-002 further confirmed a "Attended" vs "Present" discrepancy with the Data Dictionary. See Error PA-ERR-005. |
| B.4 | Were all open issues from the Analysing phase resolved before SRS finalisation? | NS | All three open issues in Analysing Report §3.5 remain unresolved in the submitted SRS. See Error PA-ERR-001. |
| B.5 | Were contradictory requirements identified during Clarify and resolved before Specifying? | NS | The 2FA scope contradiction between UR-MOB-06 and NFR-SEC-03 was not resolved. BC-01 outcomes make no reference to 2FA scope. See Error PA-ERR-003. |
| B.6 | Was the SRS reviewed for editorial quality prior to release? | PS | The SRS is generally well-structured. However, QA-USAB-01 (§5.4.1) contains an uncorrected grammatical defect (PA-ERR-007), and UR-WEB-08 and UR-WEB-09 use inconsistent capitalisation (QC-FND-010). |
| B.7 | Was the SRS formally authorised by designated BioSec stakeholders (§9 Sign-off)? | NS | All four sign-off fields in SRS §9 are blank. See Error PA-ERR-002. |
| B.8 | Was the SRS submitted at a final (≥ Version 1.0) version? | NS | SRS bears Version 0.8. See Error PA-ERR-006. |

---

### Domain C — Process Artefact Integrity

| ID | Checklist Item | Rating | Notes |
|---|---|---|---|
| C.1 | Are all required process artefacts present? (Paper Napkin Model, Context DFD, Data Dictionary, ERD, Use Case Diagram, Wireframes, iRTM, Gantt Chart) | S | All artefacts listed in SRS Table of Contents and repository README are present. Figures 1–4 and Appendices A–E confirmed. |
| C.2 | Are process artefacts internally consistent with SRS content? | PS | The Context DFD (Appendix A) documents six external entities consistent with §2.1. However, the Data Dictionary (Appendix C, Table C.4) uses attendance status values that are inconsistent with SRS §3.1 and §4.3.2 (confirmed by QC-FND-002). |
| C.3 | Do all deliverables carry a Declaration of Use of AI Tools and a Declaration on Plagiarism and Originality? | S | Both the Analysing Report (pp.3–4) and the SRS (pp.4–5 of body) carry both declarations, signed by Project Lead Loh Wen Xuan. |
| C.4 | Is the requirements repository structured correctly with all required fields per requirement? (ID, Statement, Rationale, Acceptance Criteria, Dependencies, Priority, Status) | S | Repository README confirms all seven fields per requirement. Sample review of bizops-requirements.md confirms compliance. |
| C.5 | Are Change Mitigation Strategies documented in the SRS? | S | SRS §8 documents three change mitigation strategies (CM#1: Anticipatory Contingency Requirements, CM#2: Open Issues, CM#3: High-Risk Change Control Process). |
| C.6 | Is a Risk Analysis present in the Analysing Report? | S | Analysing Report §5 documents seven risks with likelihood and impact ratings. |
| C.7 | Are version control and document metadata (version, date, document ID, prepared by) complete across all deliverables? | PS | Analysing Report (v1.0) and SRS (v0.8) both carry full metadata. SRS v0.8 is below expected release threshold (PA-ERR-006). |

---

---

## 4. QA Error Detection

The following table lists all process non-compliance instances detected during this audit. Error type for all QA findings is **Process Non-Compliance**.

| Error ID | Location | Characteristic |
|---|---|---|
| PA-ERR-001 | Analysing Report §3.5 (p.10); SRS §2.5 (p.3), §3.3 (p.6), §6.5 NFR-DOC-03 (p.16) | Three open issues documented with resolution deadlines in the Analysing phase remain unresolved in the SRS dated 11+ days after the RPO/RTO stated deadline. |
| PA-ERR-002 | SRS §9 SRS Sign-off (p.19 of SRS body) | All four designated approver fields (Name, Signature, Date) in the SRS sign-off section are blank. The SRS was presented to external audit without customer authorisation. |
| PA-ERR-003 | SRS §3.1 UR-MOB-06 (p.5); SRS §5.3 NFR-SEC-03 (p.13); Analysing Report §3.3 BC-01 outcomes (p.8) | 2FA is required of parents and teachers in UR-MOB-06 but restricted to administrators only in NFR-SEC-03. This contradiction was not identified or resolved during the Clarify phase. |
| PA-ERR-004 | SRS §4 System Features (pp.7–12); Analysing Report §3.3 BC-01 outcomes (p.8), §3.4 TC-02 outcomes (p.9); repository bizops-requirements.md | No biometric student enrolment requirement exists anywhere in the SRS or requirements repository, despite enrolment being a logical prerequisite of all scan-based operations. Analysing phase clarification sessions did not elicit this process. |
| PA-ERR-005 | SRS §3.1 UR-MOB-01 (p.5); SRS §4.3.2 (p.9); QC Report QC-FND-002 | Attendance status terminology is inconsistent across SRS sections: UR-MOB-01 uses "Attended, Absent, Late, or Excused"; §4.3.2 uses "Excused, Attended, Late, Absent." QC further confirmed "Attended" vs "Present" divergence with Data Dictionary Table C.4. Not resolved during Specifying phase. |
| PA-ERR-006 | SRS cover page; Analysing Report cover page | SRS submitted to QC/QA audit at Version 0.8 (dated 03/03/2026). The preceding Analysing Report was released at Version 1.0 (08/02/2026). The SRS was handed over before the Specifying process was completed to a final version. |
| PA-ERR-007 | SRS §5.4.1 QA-USAB-01 (p.14) | QA-USAB-01 reads: "The system shall allow parent and teacher users must be able to complete primary tasks..." The double-predicate construction ("shall allow...must be able to") is grammatically malformed and was not corrected during Specifying phase editorial review. |

---

---

## 5. QA Findings

Each finding below presents a CRaM analysis of the non-compliance instance, with evidence-based confirmation of the extent of non-compliance.

---

### PA-FND-001 — Open Issues Unresolved at SRS Finalisation

**Error ID:** PA-ERR-001
**Error Type:** Process Non-Compliance
**Severity:** High
**Process Phase:** Analysing Method — Open Issue Management; Specifying Method — SRS Finalisation

**Analysis:**

The RE process requires that open issues documented during the Analysing phase are resolved — or formally deferred with customer consent — before the SRS is finalised and released to external audit. The Analysing Report §3.5 (p.10) explicitly documents three open issues with stated deadlines:

1. **MCS Integration Security** — specific encryption handshake protocol for the MCS API. No deadline given; Nevon Solutions to coordinate with MCS vendor.
2. **Disaster Recovery RPO/RTO** — BioSec to confirm acceptable RPO and RTO for attendance data by **20 February 2026**.
3. **Biometric Template Storage Format** — confirmation on ISO/IEC 19794-2 conformance requirement.

The SRS, dated **03 March 2026** (11 days after the RPO/RTO deadline), retains all three issues as unresolved:

- SRS §2.5 (p.3): "Biometric template storage format is a pending open issue (see Appendix B). Development shall proceed with ISO/IEC 19794-2 until the open issue is resolved, with a kill date of 15 March 2026."
- SRS §3.3 (p.6), MCS External System Integration: "Encryption handshake protocol is an open issue pending MCS vendor documentation."
- SRS §6.5 NFR-DOC-03 (p.16): "Disaster recovery RPO/RTO specifications are still pending BioSec approval."

The RPO/RTO deadline of 20/02/2026 passed without resolution, and no formal deferral documentation has been presented to the QA team. The SRS was finalised and submitted for external audit with all three open issues intact. This constitutes a failure of the open issue resolution protocol required before SRS release.

**Evidence:**

| Source | Location | Content |
|---|---|---|
| Analysing Report | §3.5, p.10 | Three open issues with RPO/RTO deadline of 20/02/2026 |
| SRS | §2.5, p.3 | Biometric template storage still open; kill date 15/03/2026 |
| SRS | §3.3, p.6 | MCS encryption handshake still an open issue |
| SRS | §6.5 NFR-DOC-03, p.16 | Disaster recovery RPO/RTO "still pending BioSec approval" |

**Confirmation:** The SRS date of 03/03/2026 post-dates the RPO/RTO resolution deadline of 20/02/2026. The SRS text itself acknowledges all three issues as unresolved. No resolution or deferral documentation was presented to the QA team.

---

### PA-FND-002 — Incomplete SRS Sign-off at Time of Audit Handover

**Error ID:** PA-ERR-002
**Error Type:** Process Non-Compliance
**Severity:** High
**Process Phase:** Specifying Method — SRS Authorisation

**Analysis:**

The Specifying method requires that the completed SRS is formally reviewed and authorised by designated customer and vendor stakeholders before the document is released to external parties (QC/QA audit teams). SRS §9 (p.19 of the SRS body) provides a sign-off table that includes fields for Name, Signature, and Date for four designated roles.

The QA team reviewed SRS §9 and confirmed that all four rows in the sign-off table are entirely blank — no names, no signatures, no dates are recorded for any of the four designated approver positions. The SRS was submitted to external audit in this state. This means:

(a) No designated Nevon Solutions representative formally certified the SRS as complete before release, and
(b) No BioSec representative formally accepted the SRS as the contractual requirements baseline before the document was handed over to QC and QA teams.

The Analysing Report sign-off (p.3) is correctly completed and bears the signature of Project Lead Loh Wen Xuan dated 13/02/2026. The corresponding SRS sign-off (§9) having no completed entries indicates this authorisation step was omitted or bypassed in the Specifying process.

**Evidence:**

| Source | Location | Content |
|---|---|---|
| SRS | §9, p.19 of SRS body | Sign-off table: all four rows blank (Name, Signature, Date all empty) |
| Analysing Report | Declaration, p.3 | Correctly completed sign-off: Loh Wen Xuan, signature present, dated 13/02/2026 |

**Confirmation:** Direct inspection of SRS §9 confirms all sign-off fields are blank. By contrast, the equivalent section in the Analysing Report is correctly completed, confirming that the sign-off protocol is known to and used by the team — the omission in the SRS sign-off is therefore unexplained by process ignorance.

---

### PA-FND-003 — 2FA Scope Contradiction Not Resolved During Clarify Phase

**Error ID:** PA-ERR-003
**Error Type:** Process Non-Compliance
**Severity:** High
**Process Phase:** Analysing Method — Clarify Phase; Specifying Method — Quality Review

**Analysis:**

The Clarify phase exists to resolve all incongruities, contradictions, and ambiguities identified during Breakdown before requirements proceed to Specifying. The QC team (Veridion Labs, QC-FND-001) independently confirmed a High-severity contradiction between two 2FA requirements in the submitted SRS:

- SRS §3.1 UR-MOB-06 (p.5): "The parent and teacher authentication shall include a 2-Factor Authentication screen process."
- SRS §5.3 NFR-SEC-03 (p.13): "The system shall enforce two-factor authentication (2FA) for all administrator accounts accessing the web portal."

These two requirements are directly contradictory in scope: UR-MOB-06 mandates 2FA for parents and teachers (mobile application), while NFR-SEC-03 mandates 2FA exclusively for administrators (web portal), with no mention of parents or teachers. It is not possible for both to be correct simultaneously.

The QA team reviewed the BC-01 and TC-02 session minutes (Analysing Report §3.3–3.4, pp.8–9). The BC-01 session focused on BOR-level ambiguities relating to attendance, leave submission, notifications, and compliance thresholds. The TC-02 session addressed technical implementation boundaries. Neither session's documented outcomes contain any reference to 2FA scope, mobile authentication, or the resolution of conflicting authentication requirements.

This means the contradiction was either present in the PS and not identified during Breakdown, or was introduced during Specifying without detection. In either case, it was not resolved before the SRS was submitted for external audit.

**Evidence:**

| Source | Location | Content |
|---|---|---|
| SRS | §3.1 UR-MOB-06, p.5 | 2FA required for parents and teachers |
| SRS | §5.3 NFR-SEC-03, p.13 | 2FA required for administrators only |
| Analysing Report | §3.3 BC-01 outcomes, p.8 | No reference to 2FA scope |
| Analysing Report | §3.4 TC-02 outcomes, p.9 | No reference to 2FA scope |
| QC Report | QC-FND-001 | Independent confirmation of 2FA contradiction, classified High severity |

**Confirmation:** The SRS text of UR-MOB-06 and NFR-SEC-03 are reproduced above in full. The Analysing Report session minutes (§3.3 and §3.4) contain no documented resolution of 2FA scope. The QC team reached the same conclusion by independent inspection (QC-FND-001).

---

### PA-FND-004 — Biometric Student Enrolment Process Not Elicited

**Error ID:** PA-ERR-004
**Error Type:** Process Non-Compliance
**Severity:** High
**Process Phase:** Analysing Method — Breakdown and Clarify Phases

**Analysis:**

The Analysing method is responsible for identifying the complete set of processes that the system must support and eliciting requirements for each. The Biometric Student Attendance System's core function is biometric fingerprint-based attendance recording. This function is logically dependent on a prior enrolment process in which a student's fingerprint template is captured and registered in the system. Without enrolment, biometric verification cannot operate.

The QA team reviewed:

- SRS §4 (System Features, pp.7–12): Contains seven feature sections covering Role-Based Access Control, User Authentication, Attendance Information Access, Leave Submission, Attendance Notification, Attendance Oversight and Compliance Monitoring, and Leave and Medical Certificate Review. No enrolment feature section exists.
- Requirements repository (bizops-requirements.md, technical-requirements.md): No enrolment requirement of any kind appears in either file.
- Analysing Report §3.3 BC-01 outcomes (p.8): Documents outcomes including "biometric verification flow, notification timing logic, leave application workflow, and compliance threshold configuration." No enrolment workflow appears.
- Analysing Report §3.4 TC-02 outcomes (p.9): No reference to enrolment.

The absence of enrolment requirements from both the clarification session outcomes and the final SRS confirms that the Analysing phase did not elicit this process. Notably, BOR-0-03 in the requirements repository has an acceptance criterion that reads: "Parental consent is collected before biometric enrolment." This reference to enrolment within an acceptance criterion, without any corresponding functional requirement for the enrolment process itself, further confirms the gap: the Analysing team was aware of enrolment as a concept but did not elicit it as a requirement. The QC team independently confirmed the same omission (QC-FND-004).

**Evidence:**

| Source | Location | Content |
|---|---|---|
| SRS | §4 (pp.7–12) | No enrolment feature section; seven features documented, none covering enrolment |
| Repository | bizops-requirements.md | No enrolment requirement present |
| Repository | BOR-0-03 Acceptance Criteria | "Parental consent is collected before biometric enrolment" — references enrolment without a corresponding requirement |
| Analysing Report | §3.3 BC-01 outcomes, p.8 | No enrolment process in documented outcomes |
| Analysing Report | §3.4 TC-02 outcomes, p.9 | No enrolment process in documented outcomes |
| QC Report | QC-FND-004 | Independent confirmation of enrolment omission, classified High severity |

**Confirmation:** Exhaustive review of the SRS and requirements repository returned no enrolment requirement. The BOR-0-03 acceptance criterion references enrolment directly but no requirement covers the process. Analysing phase session minutes contain no reference to enrolment at any point. The QC team reached the same conclusion independently.

---

### PA-FND-005 — Attendance Status Terminology Inconsistency Not Resolved in Specifying Phase

**Error ID:** PA-ERR-005
**Error Type:** Process Non-Compliance
**Severity:** High
**Process Phase:** Specifying Method — Editorial Quality Review

**Analysis:**

The Specifying method requires that the SRS uses consistent terminology throughout, including alignment between the SRS body, the Data Dictionary (Appendix C), and all other artefacts. The QA team identified a terminology inconsistency in attendance status values that was not resolved before SRS submission:

- SRS §3.1 UR-MOB-01 (p.5) specifies the parent interface shall display attendance status as: **"Attended, Absent, Late, or Excused."**
- SRS §4.3.2 Stimulus/Response Sequences (p.9) states the system displays monthly records with attendance status: **"(Excused, Attended, Late, Absent)."**

The ordering and presentation of the four values differ across these two sections. The QC team (QC-FND-002) further confirmed that the Data Dictionary (Appendix C, Table C.4 AttendanceRecord) uses **"Present"** as a valid attendance_status value, which is not among the four values specified in either of the above sections. This introduces a three-way inconsistency between UR-MOB-01, §4.3.2, and the Data Dictionary — which should have been detected and unified during the Specifying phase's cross-section quality review.

**Evidence:**

| Source | Location | Content |
|---|---|---|
| SRS | §3.1 UR-MOB-01, p.5 | Attendance status: "Attended, Absent, Late, or Excused" |
| SRS | §4.3.2, p.9 | Attendance status: "Excused, Attended, Late, Absent" |
| QC Report | QC-FND-002 | Independent confirmation of "Attended" vs "Present" inconsistency with Data Dictionary Table C.4; classified High severity |

**Confirmation:** The two SRS references above are reproduced directly from the document. The QC team's independent inspection of the Data Dictionary (Appendix C) confirmed the third divergent value "Present." These inconsistencies were present in the submitted SRS at Version 0.8 and were not corrected prior to handover.

---

### PA-FND-006 — SRS Submitted Below Final Version Threshold

**Error ID:** PA-ERR-006
**Error Type:** Process Non-Compliance
**Severity:** Medium
**Process Phase:** Specifying Method — Version Control and Release Protocol

**Analysis:**

Standard version management practice in requirements engineering holds that a document submitted for external review — particularly for formal QC and QA audit — should be at a Release Candidate or Version 1.0 status. Sub-1.0 version numbers conventionally indicate that the document is in draft or under active internal revision.

The SRS cover page bears **Version 0.8**, dated **03 March 2026**. The preceding Analysing Report, which the SRS is derived from, was released at **Version 1.0** on **08 February 2026**. The gap of 23 days between the Analysing Report's release and the SRS submission, combined with the SRS carrying a sub-final version number at the point of external handover, indicates that the Specifying process was not completed to a final version before QC/QA handover.

This is corroborated by the concurrent presence of incomplete sign-off (PA-FND-002) and three unresolved open issues (PA-FND-001) in the same document — all of which are consistent with a document that had not yet completed its internal review cycle.

**Evidence:**

| Source | Location | Content |
|---|---|---|
| SRS | Cover page | Version 0.8, Date: 03 March 2026 |
| Analysing Report | Cover page | Version 1.0, Date: 08 February 2026 |

**Confirmation:** The SRS version number is directly stated on its cover page. The contrast with the completed Analysing Report version is observable from a direct comparison of the two cover pages.

---

### PA-FND-007 — Grammatical Defect in QA-USAB-01 Not Corrected by Specifying Phase Review

**Error ID:** PA-ERR-007
**Error Type:** Process Non-Compliance
**Severity:** Low
**Process Phase:** Specifying Method — Editorial Quality Review

**Analysis:**

The Specifying process is expected to include an editorial quality review of all requirement statements before SRS release, verifying that each statement is syntactically correct, clear, and unambiguous. SRS §5.4.1 contains the following requirement:

> **QA-USAB-01:** "The system shall allow parent and teacher users must be able to complete primary tasks (view attendance, submit leave requests) within three interactions from the home screen, without referring to the user manual. The interface must accommodate users with varying technical literacy."

The phrase "The system shall allow parent and teacher users **must be able to** complete..." contains a double-predicate grammatical construction. The sentence begins with "shall allow" as its modal predicate but then introduces a second predicate "must be able to" without grammatical resolution. This produces a requirement statement that is syntactically malformed and could be interpreted in two different ways regarding what the system's obligation is. The QC team independently confirmed this defect (QC-FND-009). The defect was not corrected prior to SRS submission.

**Evidence:**

| Source | Location | Content |
|---|---|---|
| SRS | §5.4.1 QA-USAB-01, p.14 | Full text reproduced above — double predicate construction |
| QC Report | QC-FND-009 | Independent confirmation of grammatical defect, classified Low severity |

**Confirmation:** The requirement text is reproduced directly from the SRS. The QC team reached the same observation independently.

---

---

## 6. Sign-Off

This QA Audit Report (PA-QAR-2026-001, Version 1.0) is submitted to BioSec Educational Institution (Customer C) by Paragon Assurance. The seven (7) process non-compliance findings documented herein represent the complete output of the QA audit of Nevon Solutions' Requirements Engineering process for the Biometric Student Attendance System. No modifications to any Nevon Solutions process artefact have been made by the QA team.

The QA team presents these findings to BioSec for review and decision.

---

| Role | Name | Signature | Date |
|---|---|---|---|
| QA Audit Lead | [QA Audit Lead Name] | ________________ | 19/03/2026 |
| QA Auditor | [QA Auditor 1 Name] | ________________ | 19/03/2026 |
| QA Auditor | [QA Auditor 2 Name] | ________________ | 19/03/2026 |
| QA Auditor | [QA Auditor 3 Name] | ________________ | 19/03/2026 |

---

---

## 7. Addenda

### Annex A — QA Team Work Allocation and Indicative Audit Timeline

#### A.1 Team Work Allocation

| Team Member | Role | Assigned Responsibilities |
|---|---|---|
| [QA Audit Lead] | QA Audit Lead | Overall audit management; Finding analysis (PA-FND-001 to PA-FND-007); Report drafting and sign-off |
| [QA Auditor 1] | QA Auditor | Domain A checklist (Analysing Method); Error detection PA-ERR-001, PA-ERR-004; Evidence consolidation |
| [QA Auditor 2] | QA Auditor | Domain B checklist (Specifying Method); Error detection PA-ERR-002, PA-ERR-003, PA-ERR-005; Evidence consolidation |
| [QA Auditor 3] | QA Auditor | Domain C checklist (Artefact Integrity); Error detection PA-ERR-006, PA-ERR-007; QC report cross-reference |

#### A.2 Indicative Audit Timeline

| Stage | Activities | Duration |
|---|---|---|
| Stage 1 | Document collection and initial review of all process artefacts | 2 hours |
| Stage 2 | QA Checklist completion across all three domains | 2 hours |
| Stage 3 | Error detection, evidence identification and documentation | 2 hours |
| Stage 4 | CRaM analysis, finding write-up, report review and sign-off | 2 hours |
| **Total** | | **~8 hours** |

---

### Glossary

| Term | Definition |
|---|---|
| QA | Quality Assurance. The process of auditing the RE process for compliance with defined process requirements. QA audits the *process*, not the work product. |
| QC | Quality Control. The process of inspecting a work product (e.g., the SRS) for authorship defects, omissions, and contradictions. QC audits the *product*, not the process. |
| RE | Requirements Engineering. The structured set of methods used to elicit, analyse, document, and validate software requirements, comprising the Analysing and Specifying methods. |
| Analysing Method | The RE method comprising Breakdown and Clarify phases, applied to the customer's Project Specification to produce a regulated-revision requirements repository ready for Specifying. |
| Specifying Method | The RE method comprising Interpret, Categorise, and Specify phases, applied to the requirements repository to produce the Software Requirements Specification (SRS). |
| Process Non-Compliance | The sole error type for QA audits. An instance where the RE process deviated from defined process requirements, either through omission, incorrect execution, or unauthorised deviation. |
| CRaM | Crisp, Realistic and Measurable. The quality criterion applied to requirements and findings to ensure they are clear, grounded in evidence, and quantifiable where applicable. |
| SRS | Software Requirements Specification. The primary work product of the Specifying method, serving as the contractual requirements baseline between customer and vendor. |
| IRC | Incongruous Requirements Checklist. The tool used during the Breakdown phase to assess each PS requirement for ambiguity, incompleteness, non-testability, technical infeasibility, and compound structure. |
| iRTM | Inceptive Requirements Traceability Matrix. The traceability artefact that establishes chain-of-custody from the Project Specification through to the SRS. |
| Open Issue | A specification matter that was identified during the Analysing phase but could not be resolved during clarification sessions, documented with a stated deadline and responsible party for resolution before SRS finalisation. |
| PDPA | Personal Data Protection Act (Singapore, 2012, as amended). The legislative framework governing the collection, use, storage, and disposal of personal data, applicable to all biometric and attendance data in this project. |

---

*End of PA-QAR-2026-001*
