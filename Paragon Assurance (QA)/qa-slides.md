---
marp: true
theme: default
paginate: true
style: |
  section {
    font-family: 'Segoe UI', Arial, sans-serif;
    font-size: 22px;
  }
  h1 { font-size: 34px; color: #1a1a2e; border-bottom: 3px solid #c0392b; padding-bottom: 8px; }
  h2 { font-size: 26px; color: #1a1a2e; }
  table { font-size: 18px; width: 100%; }
  th { background: #1a1a2e; color: white; }
  .high { color: #c0392b; font-weight: bold; }
  .medium { color: #e67e22; font-weight: bold; }
  .low { color: #27ae60; font-weight: bold; }
  footer { font-size: 14px; color: #888; }
---

<!-- Slide 1 -->
# QA Audit — Findings Presentation
## Paragon Assurance · PA-QAR-2026-001

**Vendor:** Nevon Solutions &nbsp;|&nbsp; **Customer:** BioSec Educational Institution
**Project:** P2-1561W — Biometric Student Attendance System
**Audit Period:** 15–18 March 2026 &nbsp;|&nbsp; **Auditor:** Zong Han

---

**Scope:** RE process compliance across the Analysing Method (Breakdown, Clarify) and Specifying Method (Interpret, Categorise, Specify, Finalisation)

**Overall Verdict:** RE process assessed as **substantially non-compliant**

| Severity | Count |
|---|---|
| 🔴 High | 4 |
| 🟠 Medium | 3 |
| 🟢 Low | 2 |
| **Total** | **9** |

---

<!-- Slide 2 -->
# High Severity Findings

| ID | Finding | Phase |
|---|---|---|
| PA-FND-002 | SRS circulated to external audit **before any sign-off was obtained** (document date 03/03; all signatures dated 06/03 — confirmed blank by QC at initial submission) | Specifying — Authorisation |
| PA-FND-003 | **2FA scope contradiction** between UR-MOB-06 (parents & teachers) and NFR-SEC-03 (admins only) — not identified or resolved during Clarify phase | Analysing — Clarify |
| PA-FND-004 | **Biometric student enrolment** — a logical prerequisite of all scan-based functions — was never elicited; absent from both repository and SRS entirely | Analysing — Breakdown |
| PA-FND-005 | **Three-way terminology inconsistency** for attendance status: "Attended" (UR-MOB-01) vs "Present" (Data Dictionary C.4) vs reordered list (§4.3.2) — not resolved during Specifying | Specifying — Quality Review |

---

<!-- Slide 3 -->
# Medium & Low Severity Findings

**Medium**

| ID | Finding | Phase |
|---|---|---|
| PA-FND-001 | CM-OI-03 (Biometric Template Format) **kill date 15/03 expired** on audit day 1 with no fallback activation documented; CM-OI-01 & CM-OI-02 expire 20/03 (post-audit) | Analysing — Open Issue Mgmt |
| PA-FND-006 | SRS submitted at **Version 0.8** — sub-final version handed to external QC/QA before Specifying cycle was complete | Specifying — Version Control |
| PA-FND-008 | Data Dictionary Table C.2 `fingerprint_hash` field **carries no AES-256 notation** despite NFR-SEC-01 and NFR-DB-03 requiring AES-256 for all biometric data at rest | Specifying — Cross-Artefact Consistency |

**Low**

| ID | Finding |
|---|---|
| PA-FND-007 | Double-predicate grammatical defect in QA-USAB-01 not caught by editorial review |
| PA-FND-009 | `password_hash` field in Data Dictionary specifies SHA-256 with no SRS requirement basis; incorrectly labelled "Encrypted" |

---

<!-- Slide 4 -->
# Analysis

**Two distinct failure patterns emerged:**

**1 — Analysing phase structural gaps** (PA-FND-003, PA-FND-004)
The Clarify phase did not surface a contradictory requirement that was present in the source documents, and the Breakdown phase failed to identify an entire prerequisite process (enrolment). These are not documentation errors — they represent incomplete process execution that cannot be retroactively corrected by editing the SRS.

**2 — Specifying phase process sequencing failures** (PA-FND-001, PA-FND-002, PA-FND-006)
The SRS was released to external audit before it was authorised, before it reached a final version, and with open issues whose kill dates were imminent or already past. The three findings are consistent with a document handed over before its internal review cycle was complete.

---

**On findings PA-FND-005, PA-FND-008, PA-FND-009:**
These were identified by QC (Veridion Labs) during product inspection. QA adopts them as **process evidence**: the Specifying phase's cross-artefact consistency review was insufficient to catch them before external release. The root cause is process, not authorship.

**Presented to BioSec for review and decision. No corrective actions prescribed.**
*Paragon Assurance — PA-QAR-2026-001 — 18 March 2026*
