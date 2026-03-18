---
title: "BioSec Change Request Declaration Form"
---

| | |
|---|---|
| **Form Reference** | NS-DECL-2026-001 |
| **Date Issued** | 24 February 2026 |
| **Response Due** | 1 March 2026 |
| **Issued By** | Nevon Solutions |
| **Responded By** | BioSec (Customer, P2-1561W) |

---

> **Purpose**
>
> This form is prepared by Nevon Solutions as part of their change control process for project P2-1561W (BioSec), to obtain formal customer approval for quantitative thresholds and open issue resolutions recorded in the Software Requirements Specification (SRS).
>
> A traceability review of the Project Specification (PS), Analysing Report (AR), and SRS identified:
>
> 1. Quantitative thresholds embedded in the SRS (Section A) with no documented source in the PS or AR. These represent institutional policy decisions that require formal sign-off from BioSec as the approving customer.
> 2. Open issues flagged in AR Section 3.5 and acknowledged in SRS Section 8.2 (Section B), all with kill date 15/03/2026, which has now passed without recorded resolution sign-off.
>
> BioSec is required to:
>
> - **Confirm** (Section A) that each quantitative threshold listed is correct and represents their approved institutional requirement.
> - **Accept or reject** (Section B) the resolution recorded in the SRS for each outstanding open issue.
> - **Provide explanations** in the Declaration section for any item that cannot be confirmed or is not accepted.
>
> This signed form serves as the formal customer approval record under Nevon Solutions' change control process and will be committed to the project repository by Nevon Solutions upon completion.

---

## Section A — Confirmation of SRS Quantitative Thresholds

BioSec confirms that each institutional policy value embedded in the SRS is correct and represents their approved requirements.

| Item | SRS Reference | Value Requiring Confirmation | Confirmed (Y/N) | Notes |
|---|---|---|:---:|---|
| A-01 | QA-CORRECT-01 | Attendance calculation tolerance: ±5 minutes | ☐ | |
| A-02 | BR-02 | Late arrival threshold: >15 minutes after class start | ☐ | |
| A-03 | BR-03 | Absence threshold: >50% of attendance period missed | ☐ | |
| A-04 | BR-05 | Leave approval SLA: 24 hours | ☐ | |
| A-05 | BR-06 | Medical certificate required for: >3 consecutive days absent | ☐ | |

*Tick ☐ to confirm each value is correct as stated. If any value cannot be confirmed or requires amendment, do not tick and provide the corrected value in the Declaration section below.*

---

## Section B — Open Issue Resolution

For each open issue below, BioSec confirms acceptance of the resolution recorded in the SRS. All items carried a kill date of 15/03/2026.

| Item | Open Issue | AR Reference | Resolution in SRS | Accepted (Y/N) | Notes |
|---|---|---|---|:---:|---|
| B-01 | MCS Integration Security — API key provisioning and rotation method | CM-OI-01 | Addressed via OAuth 2.0 (NFR-SEC-04); specific MCS key management deferred to implementation phase | ☐ | |
| B-02 | Disaster Recovery RPO/RTO — acceptability to institutional partners | CM-OI-02 | RPO 1 hour, RTO 4 hours as specified in NFR-SAF-04 | ☐ | |
| B-03 | Biometric Template Storage Format — NIST MINEX compliance | CM-OI-03 | Templates stored device-local only (NFR-SEC-03); NIST MINEX compliance not required given device-local model | ☐ | |

*Tick ☐ to accept the stated resolution. If a resolution is not accepted, do not tick and provide the required resolution in the Declaration section below.*

---

## Declaration

For any item in Section A where BioSec cannot confirm the stated value, or any item in Section B where BioSec does not accept the stated resolution, provide an explanation below. State the corrected value or required resolution as applicable.

| Item | Explanation / Corrected Value |
|---|---|
| | |
| | |
| | |

---

## Sign-Off

By signing below, the authorised respondent of BioSec confirms that the responses in this form are accurate and complete to the best of their knowledge. This signed form constitutes formal customer approval under Nevon Solutions' change control process.

| Name | Role | Signature | Date |
|---|---|---|---|
| | | | |

---

> **Return Instructions**
>
> The completed and signed form must be returned to Nevon Solutions by the response due date indicated above.
>
> - Nevon Solutions will retain this form as part of their change control records and commit it to the project repository.
> - Any corrected values in Section A must be reflected in a formal SRS revision issued by Nevon Solutions.
> - Any non-acceptance in Section B requires a new resolution plan to be agreed between BioSec and Nevon Solutions.
> - Items with no response by the due date will remain unresolved in Nevon Solutions' change control record.
>
> Return to: **Nevon Solutions** — designated contact.
