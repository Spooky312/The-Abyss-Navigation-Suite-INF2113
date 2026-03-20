# Requirements Engineering Process Review: Specifying Method

**Project:** Biometric Student Attendance System  
**Reviewer:** AI Assistant  
**Date:** 2026-03-20  
**Documents Reviewed:**  
1. Software Requirements Specification (SRS_1561W.pdf)  
2. Inceptive Requirements Traceability Matrix (iRTM.docx)  
3. Analysing Report (Analysing Report_1561W.pdf)  

---

## Executive Summary

This report evaluates the project's adherence to the "Specifying Method" based on the provided artefacts. Overall, the team has demonstrated a robust and well-documented process. The SRS is structured around a recognised template, and the traceability between the initial Project Specification (PS) and the final SRS is meticulously maintained through a standalone iRTM. Terminology is largely consistent, supported by a comprehensive data dictionary, and significant effort was made to resolve contradictory and ambiguous requirements during the analysis phase. However, the review has identified several critical findings that must be addressed before the SRS can be considered final and fully compliant. The most significant issues are the presence of unresolved open issues from the analysis phase carried into the SRS and the final version number of the SRS being below 1.0, which is a prerequisite for formal sign-off.

---

## Detailed Findings by Checklist Item

### B.1 — Does the SRS reference a recognised template?

- **Status:** **Present**
- **Location:** SRS, Section 1.2, Page 5
- **Evidence:** The SRS explicitly states: *"This SRS is based on the IEEE Recommended Practice for Software Requirements Specifications (IEEE Std 830-1998) template by Karl E. Wiegers."* It further notes that structural modifications were made to accommodate the project's specific methodology. This clear acknowledgment satisfies the requirement.
- **Cross-document alignment:** N/A

---

### B.2 — Are all SRS requirements traceable to earlier analysis/repository requirements via a traceability matrix?

- **Status:** **Present**
- **Location:** iRTM.docx (full document), SRS Appendix D (Pages 50-57)
- **Evidence:** The iRTM provides a comprehensive, bidirectional traceability link. Every requirement from the original Project Specification (BS-PS-2026-001) is listed and mapped to one or more corresponding, refined requirements in the SRS (NS-SRS-2026-001). A spot-check confirms this, e.g., PS requirement `BOR-1-MOB-02` is correctly traced to its decomposed atomic requirements `BOR-1-MOB-02a` and `BOR-1-MOB-02b` in the iRTM.
- **Discrepancy/Gap:** None identified. The traceability chain is complete and well-documented.
- **Cross-document alignment:** The iRTM correctly reflects the decomposition and clarification work documented in the Analysing Report (e.g., Section 2.3, Page 7). The mapping is consistent.

---

### B.3 — Does the traceability matrix exist as a standalone, extractable document?

- **Status:** **Present**
- **Location:** `iRTM.docx` (the file provided)
- **Evidence:** The iRTM is provided as a separate, complete document. It contains its own document control information (Date, Version, ID), a table of contents-like structure, and the full traceability matrix. This makes it independently usable by project stakeholders. The SRS also includes the iRTM in its Appendix D, which is good for completeness, but the existence of the standalone file fulfills the checklist item.
- **Cross-document alignment:** The standalone iRTM document is identical in content to Appendix D of the SRS, confirming alignment.

---

### B.4 — Is terminology consistent across all SRS sections and the Analysing Report?

- **Status:** **Present**
- **Location:** SRS Appendix A (Page 40), SRS Appendix C (Pages 43-49), Analysing Report Appendix C (Pages 14-19)
- **Evidence:** The SRS includes a dedicated Glossary (Appendix A) that defines key terms like `AES-256`, `FAR`, `PDPA`, etc. Furthermore, the Data Dictionary (Appendix C) rigorously defines all data fields, ensuring consistency in the system's structural terminology. A comparison of key terms like `AttendanceRecord`, `LeaveRequest`, and `BiometricScan` between the Analysing Report's Data Dictionary (Tables C.1-C.9) and the SRS's Data Dictionary shows they are identical, proving excellent cross-document consistency.
- **Cross-document alignment:** Terminology is perfectly aligned between the Analysing Report and the SRS, particularly in the Data Dictionary, which appears to have been directly carried over and refined.

---

### B.5 — Were all open issues from the analysis phase resolved before SRS finalisation?

- **Status:** **Missing / Non-Compliant**
- **Location:** Analysing Report Section 3.5 (Page 10), SRS Section 2.7 (Page 8), SRS Section 8.2 (Page 21), SRS Appendix B (Page 42)
- **Evidence:** The Analysing Report (Section 3.5) explicitly lists three open issues: MCS Integration Security, Disaster Recovery RPO/RTO, and Biometric Template Storage Format.
    - The SRS has not resolved these issues. Instead, it has formalised them in a new section, "CM#2: Open Issues" (Section 8.2) and listed them again in "Appendix B - Issues List".
    - These issues are also flagged as assumptions/dependencies (SRS Section 2.7) and in the relevant functional requirements (e.g., FR-SW-01). While the "kill dates" and fallback plans are a strong mitigation strategy, the issues remain *open* in the final SRS.
- **Discrepancy/Gap:** This is the most critical finding. A final SRS, by definition, should have all requirements agreed upon and resolved. Carrying forward open issues from analysis creates significant project risk. The process of "specifying" should be complete before finalisation.
- **Recommendation:** The project must be instructed that an SRS with open issues (CM-OI-01, CM-OI-02, CM-OI-03) cannot be considered a "final" specification. These must be closed or the SRS version must be marked as a draft (e.g., 0.9) to reflect its true status.

---

### B.6 — Were contradictory requirements identified and resolved before specifying?

- **Status:** **Present**
- **Location:** Analysing Report Section 2.2 (Page 4), Section 3.3 (Page 8), Section 3.4 (Page 9)
- **Evidence:** The Analysing Report provides strong evidence of a structured process to identify and resolve contradictions.
    1.  **Identification:** Section 2.2 explicitly lists "Incongruent Requirements," including "Technically Infeasible Requirements" such as the unrealistic `FAR 0.001%` from `TR-1-BE-04`.
    2.  **Resolution:** Section 3.4 (Technical Requirements Clarification Session) documents the resolution: *"FAR target revised to 0.01% based on commercial sensor capabilities..."*.
    3.  **Final State:** The SRS reflects this resolved value. In the iRTM, the mapping for `TR-1-BE-04` links to `FR-HW-02` and `FR-HW-03`, which correctly state the performance targets without referencing the unrealistic FAR value. This demonstrates a clear path from contradiction to resolution.
- **Cross-document alignment:** The three documents tell a coherent story of conflict identification (AR), stakeholder resolution (AR), and final agreed-upon specification (SRS/iRTM).

---

### B.9 — Was the SRS submitted at a final version level (≥ Version 1.0)?

- **Status:** **Missing / Non-Compliant**
- **Location:** SRS Cover Page (Page 1)
- **Evidence:** The SRS cover page clearly states: **"Version: 0.8"**. The document is also dated 3 March 2026. For a document intended to serve as the "primary contractual basis for design, development, testing, and delivery" and to be formally signed off (Section 9), a version below 1.0 is inappropriate. It implies the document is still a draft and not yet a final, stable baseline.
- **Discrepancy/Gap:** There is a fundamental mismatch between the document's stated purpose and its version number. This is compounded by the presence of open issues (B.5), which further confirms that version 0.8 is not a final specification. The project appears to have conflated "submitted for approval" with "final." A version 0.8 document is submitted *for review*, not *for sign-off as the final baseline*.
- **Recommendation:** This is the second critical finding. The SRS must be advanced to version 1.0 *after* all open issues are resolved and the document is formally baselined. The current version 0.8 is pre-final.

---

## Summary of Findings

| Item | Status | Key Evidence Location | Notes |
| :--- | :--- | :--- | :--- |
| **B.1** | Present | SRS §1.2 | Explicitly references IEEE 830-1998. |
| **B.2** | Present | iRTM.docx, SRS Appendix D | Full traceability from PS to SRS is maintained. |
| **B.3** | Present | `iRTM.docx` file | The iRTM exists as a complete, standalone document. |
| **B.4** | Present | SRS Appendix A & C, AR Appendix C | Terminology is highly consistent, with a shared data dictionary. |
| **B.5** | **Missing** | AR §3.5, SRS §8.2, SRS App. B | **Critical:** Open issues from analysis were NOT resolved and were carried into the SRS. |
| **B.6** | Present | AR §2.2, §3.4; SRS iRTM | Clear evidence of identifying and resolving contradictions (e.g., FAR target). |
| **B.9** | **Missing** | SRS Cover Page | **Critical:** SRS version is 0.8, which is below the 1.0 threshold for a final specification. |

---

## Overall Conclusion

The project team has executed a technically sound requirements engineering process, with excellent documentation of analysis, traceability, and consistency. The Analysing Report is a model of clarity, and the iRTM ensures a clear line-of-sight from the customer's original requests to the final specification.

However, the **Specifying method has not been fully completed.** The presence of open issues (CM#2) and a version number below 1.0 indicates that the SRS is still a draft, not a final, baselined document. Submitting a version 0.8 document for final sign-off creates significant contractual and project risk. The "Change Mitigation Strategies" (Section 8) are forward-thinking, but they are designed to manage *future* changes to a *baselined* SRS, not to excuse *current* incomplete requirements.

**Final Recommendation:** The review cannot approve the SRS in its current state. The project must be directed to close all open issues (CM-OI-01, -02, -03) with BioSec, update the SRS accordingly, and then re-submit it as **Version 1.0** for final approval and sign-off. The current document should be re-categorised as a draft for review.