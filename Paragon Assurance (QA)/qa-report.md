# PARAGON ASSURANCE
## Quality Assurance Audit Report
### Requirements Engineering Process — Biometric Student Attendance System

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
- QC Audit Report, Veridion Labs (QC), as provided to the QA auditor
- Requirements repository artefacts (GitHub: https://github.com/wenxuannx/Biometric-Student-Attendance-System)
- Clarification session minutes: BC-01 (07/02/2026) and TC-02 (09/02/2026)

### 1.2 Audit Goals

The QA audit was conducted to establish the degree of compliance of Nevon Solutions' RE process with the process requirements applicable to the Analysing and Specifying methods, and to identify any instances of process non-compliance that may affect the completeness, correctness, or authorisation status of the deliverables presented to BioSec.

### 1.3 Summary of Findings

The audit identified **nine (9) process non-compliance instances**. Three (3) are classified as High severity, two (2) as Medium severity, two (2) as Medium-Low severity, and two (2) as Low severity. Key non-compliance areas are:

- The SRS sign-off section (§9) was initially submitted to QC/QA audit with all designated approver fields blank. Sign-off was subsequently obtained on 06/03/2026 — three days after the document date — confirming the SRS was circulated externally before formal authorisation was in place.
- One of three formally deferred open issues (CM-OI-03, Biometric Template Format, kill date 15/03/2026) expired on the first day of the audit period (15/03/2026) without documented resolution or confirmed fallback activation. Two further open issues (CM-OI-01, CM-OI-02) expire on 20/03/2026, two days after the audit close date.
- A contradictory 2FA scope specification was not resolved during the Clarify phase.
- The biometric student enrolment process — a prerequisite for all scan-based system functions — was not elicited during the Analysing phase and is entirely absent from the SRS.
- A cross-section attendance status terminology inconsistency was not detected or corrected during the Specifying phase, confirmed directly by Data Dictionary Table C.4 (status field: Present, Late, Absent, Excused) diverging from SRS §3.1 UR-MOB-01 (Attended, Absent, Late, or Excused).
- The SRS was submitted at Version 0.8, below the Version 1.0 threshold expected for a document released to external audit.
- A grammatical defect in requirement QA-USAB-01 was not corrected by the Specifying phase editorial review.
- Data Dictionary Table C.2 specifies the biometric fingerprint field without indicating the AES-256 encryption mandated by SRS NFR-SEC-01 and NFR-DB-03, indicating the Specifying phase did not verify cross-artefact security consistency.
- Data Dictionary Table C.1 introduces a specific password storage technology (SHA-256) for the password_hash field without backing from any SRS requirement, constituting an unauthorised design decision embedded in a requirements artefact.

The QA auditor presents these findings without amendment to BioSec for review and decision.

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

| Phase | Activities | Assignee |
|---|---|---|
| Phase 1: Document Review | Review of all process artefacts; Analysing Report, SRS, QC report, repository | Zong Han |
| Phase 2: Checklist Assessment | Completion of QA Checklist against each process phase | Zong Han |
| Phase 3: Error Detection & Evidence | Identification and documentation of non-compliance instances | Zong Han |
| Phase 4: Finding Analysis & Sign-off | CRaM analysis, evidence consolidation, report finalisation | Zong Han |

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
| A.6 | Were open issues formally deferred with kill dates and fallback mechanisms documented? | PS | Three open issues formally deferred via SRS §8.2 CM#2 with kill dates and fallbacks; BioSec signed off on SRS inclusive of these (06/03/2026). However, CM-OI-03 kill date (15/03/2026) has passed without documented fallback activation. See Error PA-ERR-001. |
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
| B.7 | Was the SRS formally authorised by designated BioSec stakeholders (§9 Sign-off) before external handover? | PS | Updated SRS §9 shows full sign-off (5 parties, dated 06/03/2026). However, the SRS document date is 03/03/2026 and QC-FND-011 confirmed sign-off was blank at initial submission. Sign-off obtained 3 days after document date and after external audit had begun. See Error PA-ERR-002. |
| B.8 | Was the SRS submitted at a final (≥ Version 1.0) version? | NS | SRS bears Version 0.8. See Error PA-ERR-006. |

---

### Domain C — Process Artefact Integrity

| ID | Checklist Item | Rating | Notes |
|---|---|---|---|
| C.1 | Are all required process artefacts present? (Paper Napkin Model, Context DFD, Data Dictionary, ERD, Use Case Diagram, Wireframes, iRTM, Gantt Chart) | S | All artefacts listed in SRS Table of Contents and repository README are present. Figures 1–4 and Appendices A–E confirmed. |
| C.2 | Are process artefacts internally consistent with SRS content? | NS | Three inconsistencies confirmed from direct Data Dictionary inspection: (1) Table C.4 status ENUM uses "Present, Late, Absent, Excused" while SRS §3.1 uses "Attended"; (2) Table C.2 fingerprint_hash field carries no AES-256 encryption specification despite NFR-SEC-01 and NFR-DB-03; (3) Table C.1 password_hash field specifies SHA-256 with no SRS requirement basis. See Errors PA-ERR-005, PA-ERR-008, PA-ERR-009. |
| C.3 | Do all deliverables carry a Declaration of Use of AI Tools and a Declaration on Plagiarism and Originality? | S | Both the Analysing Report (pp.3–4) and the SRS (pp.4–5 of body) carry both declarations, signed by Project Lead Loh Wen Xuan. |
| C.4 | Is the requirements repository structured correctly with all required fields per requirement? (ID, Statement, Rationale, Acceptance Criteria, Dependencies, Priority, Status) | S | Repository README confirms all seven fields per requirement. Sample review of bizops-requirements.md confirms compliance. |
| C.5 | Are Change Mitigation Strategies documented in the SRS? | S | SRS §8 documents three change mitigation strategies (CM#1: Anticipatory Contingency Requirements, CM#2: Open Issues, CM#3: High-Risk Change Control Process). |
| C.6 | Is a Risk Analysis present in the Analysing Report? | S | Analysing Report §5 documents seven risks with likelihood and impact ratings. |
| C.7 | Are version control and document metadata (version, date, document ID, prepared by) complete across all deliverables? | PS | Analysing Report (v1.0) and SRS (v0.8) both carry full metadata. SRS v0.8 is below expected release threshold (PA-ERR-006). |
| C.8 | Do all Data Dictionary fields containing biometric data include explicit AES-256 encryption notation consistent with SRS security requirements? | NS | Table C.2 fingerprint_hash field describes the biometric field as a "hash" with no AES-256 encryption specification. NFR-SEC-01 and NFR-DB-03 require AES-256 for all biometric data at rest. See Error PA-ERR-008. |
| C.9 | Are Data Dictionary field descriptions free of technology or algorithm choices not backed by SRS requirements? | NS | Table C.1 password_hash field specifies "SHA256 hash" — a specific algorithm choice with no SRS backing. Description also incorrectly uses "Encrypted" to describe a hash function. See Error PA-ERR-009. |

---

---

## 4. QA Error Detection

The following table lists all process non-compliance instances detected during this audit. Error type for all QA findings is **Process Non-Compliance**.

| Error ID | Location | Characteristic |
|---|---|---|
| PA-ERR-001 | Analysing Report §3.5 (p.10); SRS §8.2 CM#2 table (p.18); SRS §2.5 (p.3), §6.5 NFR-DOC-03 (p.16) | Three open issues were formally deferred into SRS via CM#2 with kill dates. CM-OI-03 (Biometric Template Format, kill date 15/03/2026) expired on the first day of the audit period (15/03/2026) with no resolution or confirmed fallback activation documented. CM-OI-01 and CM-OI-02 expire 20/03/2026, two days after audit close. |
| PA-ERR-002 | SRS §9 (p.19 of SRS body); QC Report QC-FND-011; SRS cover page (03/03/2026) vs sign-off date (06/03/2026) | The SRS was initially submitted to QC/QA with all sign-off fields blank (confirmed by QC-FND-011). Sign-off was subsequently completed on 06/03/2026 — three days after the SRS document date — indicating the SRS was circulated externally before formal authorisation was obtained. |
| PA-ERR-003 | SRS §3.1 UR-MOB-06 (p.5); SRS §5.3 NFR-SEC-03 (p.13); Analysing Report §3.3 BC-01 outcomes (p.8) | 2FA is required of parents and teachers in UR-MOB-06 but restricted to administrators only in NFR-SEC-03. This contradiction was not identified or resolved during the Clarify phase. |
| PA-ERR-004 | SRS §4 System Features (pp.7–12); Analysing Report §3.3 BC-01 outcomes (p.8), §3.4 TC-02 outcomes (p.9); repository bizops-requirements.md | No biometric student enrolment requirement exists anywhere in the SRS or requirements repository, despite enrolment being a logical prerequisite of all scan-based operations. Analysing phase clarification sessions did not elicit this process. |
| PA-ERR-005 | SRS §3.1 UR-MOB-01 (p.5); SRS §4.3.2 (p.9); Data Dictionary Table C.4 (status ENUM: Present, Late, Absent, Excused) | Attendance status terminology is inconsistent: UR-MOB-01 uses "Attended, Absent, Late, or Excused"; §4.3.2 uses "Excused, Attended, Late, Absent"; Data Dictionary Table C.4 status ENUM uses "Present" — not "Attended." Three-way inconsistency not resolved during Specifying phase. |
| PA-ERR-006 | SRS cover page; Analysing Report cover page | SRS submitted to QC/QA audit at Version 0.8 (dated 03/03/2026). The preceding Analysing Report was released at Version 1.0 (08/02/2026). The SRS was handed over before the Specifying process was completed to a final version. |
| PA-ERR-007 | SRS §5.4.1 QA-USAB-01 (p.14) | QA-USAB-01 reads: "The system shall allow parent and teacher users must be able to complete primary tasks..." The double-predicate construction ("shall allow...must be able to") is grammatically malformed and was not corrected during Specifying phase editorial review. |
| PA-ERR-008 | Data Dictionary Table C.2 Student (fingerprint_hash field); SRS §5.3 NFR-SEC-01 (p.13); SRS §6.1 NFR-DB-03 (p.15) | Data Dictionary Table C.2 describes the fingerprint_hash field as "Biometric hash for attendance matching" with no indication of AES-256 encryption. SRS NFR-SEC-01 and NFR-DB-03 both require biometric data to be encrypted with AES-256 at rest. The Specifying phase did not verify that the Data Dictionary reflected the SRS's mandatory security requirements. |
| PA-ERR-009 | Data Dictionary Table C.1 UserAccount (password_hash field); SRS §4–§6 (no password hashing requirement) | Data Dictionary Table C.1 describes the password_hash field as "Encrypted password (SHA256 hash)". No SRS requirement specifies SHA-256 as the password storage algorithm. SHA-256 is also incorrectly described as "Encrypted" (it is a hash function). A specific technology choice was introduced into the requirements artefact without SRS basis. |

---

---

## 5. QA Findings

Each finding below presents a CRaM analysis of the non-compliance instance, with evidence-based confirmation of the extent of non-compliance.

---

### PA-FND-001 — CM-OI-03 Kill Date Expired; CM-OI-01 and CM-OI-02 Imminent

**Error ID:** PA-ERR-001
**Error Type:** Process Non-Compliance
**Severity:** Medium
**Process Phase:** Analysing Method — Open Issue Management; Specifying Method — CM#2 Protocol

**Analysis:**

The Analysing Report §3.5 (p.10) documented three open issues that could not be resolved during clarification sessions. In the SRS, these were formally codified as CM#2 (Open Issues) items in §8.2 (p.17–18), each assigned a kill date and fallback mechanism. The BioSec sign-off on the SRS (06/03/2026) confirms BioSec accepted the SRS inclusive of these open issues and their kill dates. The CM#2 mechanism in itself represents a legitimate process instrument for managing unresolved issues.

However, the following non-compliance is noted as of the audit close date (18/03/2026):

**CM-OI-03 (Biometric Template Storage Format) — Kill date 15 March 2026 — EXPIRED:**
The kill date of 15/03/2026 fell on the first day of the audit period. Per SRS §8.2, "if not resolved by that date, the fallback action takes effect." The stated fallback for CM-OI-03 is: "ISO/IEC 19794-2 as default for interoperability." No documentation of the fallback activation was presented to the QA auditor at any point during the audit period (15–18/03/2026). The process requires that when a kill date passes, the fallback is formally activated and the iRTM updated (per SRS §8.2 and §7). Neither has been evidenced.

**CM-OI-01 (MCS Integration Security) — Kill date 20 March 2026:**
This open issue expires two days after the audit close date. No resolution or pre-resolution communication was presented to the QA auditor during the audit period.

**CM-OI-02 (Disaster Recovery RPO/RTO) — Kill date 20 March 2026:**
This open issue also expires two days after the audit close date. No resolution was presented during the audit period.

The Analysing Report §3.5 originally stated the RPO/RTO deadline as 20/02/2026. The SRS CM#2 table extended this to 20/03/2026. While the BioSec sign-off on the SRS implies acceptance of the new kill dates, no formal deferral or extension document for the original Analysing Report deadline was independently presented to the QA auditor.

**Evidence:**

| Source | Location | Content |
|---|---|---|
| Analysing Report | §3.5, p.10 | Three open issues; RPO/RTO stated deadline 20/02/2026 |
| SRS | §8.2 CM#2 table, p.17–18 | CM-OI-01: kill 20/03/2026; CM-OI-02: kill 20/03/2026; CM-OI-03: kill 15/03/2026 |
| SRS | §2.5, p.3 | Biometric template format open; kill date 15/03/2026 |
| SRS | §6.5 NFR-DOC-03, p.16 | RPO/RTO "still pending BioSec approval" |
| SRS | §9, p.19 | BioSec signed off on SRS "inclusive of open issues" on 06/03/2026 |

**Confirmation:** The CM-OI-03 kill date of 15/03/2026 coincides with the first day of the audit period (15/03/2026). The SRS CM#2 table and SRS §2.5 text are reproduced in evidence above. No fallback activation documentation was presented at any point during the audit period. CM-OI-01 and CM-OI-02 expire on 20/03/2026, two days after the audit close date of 18/03/2026.

---

### PA-FND-002 — SRS Circulated to External Audit Before Sign-off Was Obtained

**Error ID:** PA-ERR-002
**Error Type:** Process Non-Compliance
**Severity:** High
**Process Phase:** Specifying Method — SRS Authorisation and Release Protocol

**Analysis:**

The Specifying method requires that the completed SRS is formally reviewed and authorised by designated stakeholders before the document is released to external parties. The updated SRS §9 (p.19) now shows a completed sign-off table with five signatories across two parties:

**Vendor Authenticator:** Loh Wen Xuan (Project Lead), signed, dated 06/03/2026
**Designated Approvers – Vendor (Nevon Solutions):**
- Technical Lead: James Koh, signed, dated 06/03/2026
- System Architect Lead: Rachel Lee, signed, dated 06/03/2026

**Designated Approvers – Customer (BioSec):**
- Project Manager: Marcus Tan Wei Liang, signed, dated 06/03/2026
- Head of Operations: Daniel Rodriguez, signed, dated 06/03/2026

The sign-off is complete and genuine in the updated version. However, the process non-compliance lies in the sequence of events:

1. The SRS cover page bears the document date of **03/03/2026**.
2. All five sign-off dates are **06/03/2026** — three days later.
3. The QC team (Veridion Labs) independently confirmed that the SRS sign-off section was blank at the time of their inspection (QC-FND-011), which aligns with the initial version of the SRS having no sign-off.
4. The git repository for the customer's BioSec system shows the SRS was subsequently updated (commit: "Update SRS_1561W.pdf"), with the sign-off-complete version uploaded after the initial blank-sign-off version.

This sequence confirms that: (a) the SRS was prepared and submitted to external QC/QA on or around 03/03/2026 without any sign-off, and (b) sign-off from both vendor and customer parties was obtained on 06/03/2026 and the document updated retroactively. The process requires sign-off before external release — not after.

Additionally, the SRS §9 preamble states "By signing below, **the Project Lead** certifies the following..." but the sign-off structure includes two vendor approvers and two BioSec approvers beyond the Project Lead. The preamble is inconsistent with the multi-party sign-off structure.

**Evidence:**

| Source | Location | Content |
|---|---|---|
| SRS (updated) | §9, p.19 of SRS body | All five sign-off fields completed; all dated 06/03/2026 |
| SRS cover page | Cover | Document date: 03/03/2026 — three days before sign-off |
| QC Report | QC-FND-011 | Independent confirmation: sign-off was blank at time of QC inspection |
| Git repository | Commit: "Update SRS_1561W.pdf" | SRS updated after initial submission, consistent with sign-off being added post-release |
| Analysing Report | Declaration, p.3 | Correctly completed sign-off prior to release: Loh Wen Xuan, dated 13/02/2026 |

**Confirmation:** The three-day gap between the SRS document date (03/03) and all sign-off dates (06/03), combined with QC-FND-011's independent observation of blank sign-off fields and the git repository's subsequent update commit, together confirm that the SRS was released to external audit before formal authorisation was obtained from any party.

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
| Data Dictionary | Table C.4 AttendanceRecord, status field | ENUM defined as: "Present, Late, Absent, Excused" — uses "Present", not "Attended" |
| QC Report | QC-FND-002 | Independent confirmation of "Attended" vs "Present" inconsistency; classified High severity |

**Confirmation:** All three sources are directly observable. The Data Dictionary Table C.4 status ENUM definition — "Present, Late, Absent, Excused" — was read directly from the repository file `data-dictionary.md` and contains "Present" as the first valid status value. This confirms a three-way inconsistency across the SRS body and the Data Dictionary that was not resolved during the Specifying phase.

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

### PA-FND-008 — Data Dictionary fingerprint_hash Field Lacks Mandatory AES-256 Encryption Specification

**Error ID:** PA-ERR-008
**Error Type:** Process Non-Compliance
**Severity:** Medium
**Process Phase:** Specifying Method — Cross-Artefact Consistency Review

**Analysis:**

The Specifying method requires that supporting artefacts — including the Data Dictionary — are consistent with the SRS requirements. Two SRS requirements explicitly mandate AES-256 encryption for biometric data at rest:

- **SRS §5.3 NFR-SEC-01** (p.13): "The system shall encrypt biometric data, including fingerprint templates, at rest using AES-256 and in transit using TLS 1.2 or higher. No plaintext biometric data shall be stored or transmitted at any point."
- **SRS §6.1 NFR-DB-03** (p.15–16): "All biometric template data in the database to be encrypted with AES-256. No plaintext biometric data shall be written to the database at any time."

The Data Dictionary Table C.2 – Student defines the following field:

| Field Name | Data Type | Description | Example |
|---|---|---|---|
| fingerprint_hash | VARCHAR(256) | Biometric hash for attendance matching | (hash) |

The field description states "Biometric hash for attendance matching" and carries no indication of AES-256 encryption. The field is named `fingerprint_hash` — a "hash" is a one-way transformation, which is a fundamentally different operation from AES-256 encryption, which is reversible. The two SRS requirements above require the biometric data to be *encrypted* (AES-256), not merely *hashed*. The Data Dictionary entry for this field does not reflect the SRS's encryption mandate.

The Specifying phase should have verified that all Data Dictionary fields containing biometric data included explicit notation of AES-256 encryption consistent with NFR-SEC-01 and NFR-DB-03. This consistency check was not performed or was inadequate.

**Evidence:**

| Source | Location | Content |
|---|---|---|
| Data Dictionary | Table C.2 Student, fingerprint_hash field | "Biometric hash for attendance matching" — no AES-256 encryption specified; field named as hash not encrypted value |
| SRS | §5.3 NFR-SEC-01, p.13 | "encrypt biometric data, including fingerprint templates, at rest using AES-256... No plaintext biometric data shall be stored" |
| SRS | §6.1 NFR-DB-03, p.15–16 | "All biometric template data in the database to be encrypted with AES-256" |

**Confirmation:** The Data Dictionary file `data-dictionary.md` was read directly from the repository. Table C.2's fingerprint_hash field contains no AES-256 notation. NFR-SEC-01 and NFR-DB-03 are reproduced from the SRS above and unambiguously require AES-256 for biometric data at rest. The discrepancy between the Data Dictionary's field description and the SRS security requirements is directly observable.

---

### PA-FND-009 — Data Dictionary Introduces Unspecified Technology Decision for Password Storage

**Error ID:** PA-ERR-009
**Error Type:** Process Non-Compliance
**Severity:** Low
**Process Phase:** Specifying Method — Requirements Artefact Quality Control

**Analysis:**

The Data Dictionary is a requirements modelling artefact produced during the Analysing phase and embedded in the SRS as Appendix C. As a requirements artefact, it should specify data structures and field semantics at the requirements level — consistent with SRS requirements — without introducing technology or algorithm choices that have no requirements basis.

Data Dictionary Table C.1 – UserAccount defines the following field:

| Field Name | Data Type | Description | Example |
|---|---|---|---|
| password_hash | VARCHAR(256) | Encrypted password (SHA256 hash) | (hash) |

This entry introduces **SHA-256** as the specific algorithm for password storage. The QA team reviewed the entirety of the SRS (Sections 1–8, Appendices A–E) and confirms that no SRS requirement specifies SHA-256, or any other hashing or encryption algorithm, for user password storage. The SRS §5.3 security requirements address biometric data encryption (NFR-SEC-01), MCS API authentication (NFR-SEC-05), and account lockout (NFR-SEC-04), but are silent on password storage algorithms.

Additionally, the field description uses the term "Encrypted password" to describe a SHA-256 hash. SHA-256 is a cryptographic hash function — a one-way operation — and is not encryption. The description is technically inaccurate. This inaccuracy in a requirements artefact introduces ambiguity about whether the stored value is a hash or an encrypted (and therefore decryptable) value.

The Specifying phase's quality review of the Data Dictionary did not identify that Table C.1 contained an unspecified algorithm choice and an incorrect technical descriptor.

**Evidence:**

| Source | Location | Content |
|---|---|---|
| Data Dictionary | Table C.1 UserAccount, password_hash field | "Encrypted password (SHA256 hash)" — specifies SHA-256 with no SRS basis; incorrectly describes SHA-256 as "Encrypted" |
| SRS | §4–§6, all security requirements | Full review: no requirement mandates any password hashing or storage algorithm |

**Confirmation:** The Data Dictionary file `data-dictionary.md` was read directly from the repository. Table C.1's password_hash field contains the string "SHA256 hash." A review of all SRS security requirements (NFR-SEC-01 through NFR-SEC-09, §5.3) returns no reference to SHA-256 or any password hashing specification.

---

---

## 6. Sign-Off

This QA Audit Report (PA-QAR-2026-001, Version 1.0) is submitted to BioSec Educational Institution (Customer C) by Paragon Assurance. The nine (9) process non-compliance findings documented herein represent the complete output of the QA audit of Nevon Solutions' Requirements Engineering process for the Biometric Student Attendance System. No modifications to any Nevon Solutions process artefact have been made by the QA auditor.

The QA auditor presents these findings to BioSec for review and decision.

---

| Role | Name | Signature | Date |
|---|---|---|---|
| QA Auditor | Zong Han | ________________ | 18/03/2026 |

---

---

## 7. Addenda

### Annex A — QA Team Work Allocation and Indicative Audit Timeline

#### A.1 Auditor

| Name | Role | Responsibilities |
|---|---|---|
| Zong Han | QA Auditor | Full audit: document review, checklist assessment (Domains A–C), error detection (PA-ERR-001 to PA-ERR-009), finding analysis, report drafting and sign-off |

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
