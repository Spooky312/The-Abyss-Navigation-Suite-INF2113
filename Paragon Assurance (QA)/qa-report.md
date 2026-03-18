# QA Findings Report

**Paragon Assurance --- Quality Assurance Audit**

  -----------------------------------------------------------------------
  Field                               Details
  ----------------------------------- -----------------------------------
  **Report Reference**                PA-QA-2026-002

  **Checklist Reference**             PA-QA-2026-002-CL

  **Customer (Vendor under audit)**   Nevon Solutions

  **End Customer**                    BioSec Educational Institution

  **Project ID**                      P2-1561W

  **Subject**                         Requirements Engineering (RE)
                                      Process --- Biometric Student
                                      Attendance System

  **Auditor**                         Paragon Assurance

  **Report Date**                     18 March 2026

  **SRS Version Reviewed**            0.8 (NS-SRS-2026-001, dated 3 March
                                      2026)

  **Analysing Report Version          1.0 (NS-AR-2026-001, dated 8
  Reviewed**                          February 2026)

  **IRC Version Reviewed**            NS-IRC-2026-001, dated 8 February
                                      2026
  -----------------------------------------------------------------------

## 1. Executive Summary

Paragon Assurance conducted a quality assurance audit of the
Requirements Engineering (RE) process performed by Nevon Solutions for
BioSec Educational Institution (Project ID: P2-1561W) in connection with
the development of a Biometric Student Attendance System. The audit
covered three RE phases: Analysing, Specifying, and Validating.

The audit examined 14 process checklist items across Nevon's RE phases,
plus three items attributable to the external QC team. Of the 14 Nevon
items, eleven passed with confirmed documentary evidence and one could
not be fully confirmed. Of the three QC team items, all three resulted
in non-conformances due to the absence of expected artefacts. QC team
findings are reported separately in Section 6.

The Analysing and Specifying phases were found to be complete and
well-evidenced. All seven Analysing items and all four Specifying items
were confirmed as passing, with artefacts traceable in the repository.
The Validating phase presents areas of concern: no documentary evidence
of editorial checks was found. The customer sign-off on the SRS has
since been confirmed via the BioSec Change Request Declaration Form
(NS-DECL-2026-001) committed to the repository; NC-01 is resolved.

No solutions or corrective actions are proposed in this report. The
findings are presented as a factual record of the process state as
observed.

## 2. Scope and Methodology

### 2.1 Scope

This audit covers the Analysis, Specifying, and Validating phases of the
RE process conducted by Nevon Solutions. The Eliciting phase, performed
by BioSec Educational Institution, is outside the scope of this audit.
This audit examines process completeness and flow --- not the content
quality of individual requirements, which is the domain of the assigned
QC team.

### 2.2 Methodology

The audit was conducted through document review of all artefacts
accessible in the Nevon Solutions project repository. Evidence was
examined against the checklist (PA-QA-2026-002-CL). Where artefacts were
absent or partially verified, the finding is recorded with the specific
gap identified.

The following primary source artefacts were examined:

  -------------------------------------------------------------------------------------
  Artefact                Document ID / File                    Date
  ----------------------- ------------------------------------- -----------------------
  Analysing Report        `NS-AR-2026-001` /                    8 Feb 2026
                          `Analysing Report_1561W.pdf`

  Incongruous             `NS-IRC-2026-001` /                   8 Feb 2026
  Requirements Checklist  `IRC_Nevon_Solutions.pdf`

  Project Specification   `BS-PS-2026-001` /                    Prior to analysis
                          `Project Specification_1561W.pdf`

  Software Requirements   `NS-SRS-2026-001` / `SRS_1561W.pdf`   3 Mar 2026
  Specification

  iRTM                    `iRTM.docx`                           ---

  Change Request Form     `Change Request Form Template.docx`   ---
  Template

  Gantt Chart             `BioSec Gantt Chart.xlsx`             ---

  IEEE SRS Template       `srs_template-ieee.doc`               ---

  Requirements files      `bizops-requirements.md`,             ---
                          `technical-requirements.md`

  Context Diagram         `context-diagram.pdf`                 ---
  (Revised)

  Paper Napkin Model      `paper-napkin-model.jpg`              ---
  -------------------------------------------------------------------------------------

## 3. Analysing Phase --- Findings

  -----------------------------------------------------------------------
  ID      Checklist Item                        Status   Evidence / Notes
  ------- ------------------------------------- -------- ----------------
  A-01    PS in repository                       Pass     `documents/Project Specification_1561W.pdf`

  A-02    Plan for analysis phase                Pass     `BioSec Gantt Chart.xlsx`; structured sessions BC-01, TC-02

  A-03    Models carried forward from PS         Pass     `paper-napkin-model.jpg`, `context-diagram.pdf`

  A-04    Models revised; originals retained     Pass     Revised: `context-diagram.pdf`, AR Appendix B; original in PS

  A-05    Requirements codified with unique IDs  Pass     BOR/TR scheme; `iRTM.docx`

  A-06    IRC exists as standalone document      Pass     `documents/IRC_Nevon_Solutions.pdf`

  A-07    IRC was used / filled in               Pass     9 categories completed with project-specific findings
  -----------------------------------------------------------------------

## 4. Specifying Phase --- Findings

  -----------------------------------------------------------------------
  ID      Checklist Item                                   Status   Evidence / Notes
  ------- ------------------------------------------------ -------- ----------------
  S-01    SRS references a recognised template              Pass     IEEE Std 830-1998 (Wiegers); `srs_template-ieee.doc` in repo

  S-02    All repository requirements accounted for in SRS  Pass     SRS Sections 4--6; iRTM chain of custody

  S-03    iRTM as a standalone extractable file             Pass     `documents/iRTM.docx`

  S-04    Change management template exists                 Pass     `requirement-models/Change Request Form Template.docx`
  -----------------------------------------------------------------------

## 5. Validating Phase --- Nevon Findings

  -----------------------------------------------------------------------
  ID      Checklist Item                        Status    Evidence / Notes
  ------- ------------------------------------- --------- ----------------
  V-01    Requirements change documentation      Pass      NS-DECL-2026-001 committed to repository; 5 thresholds and 3 open issues confirmed by BioSec

  V-02    Editorial checks performed on SRS      Partial   No documentary evidence found; SRS Declaration page does not record checks as a distinct activity
  -----------------------------------------------------------------------

## 6. QC Team Findings

  -----------------------------------------------------------------------
  ID      Checklist Item                        Status   Evidence / Notes
  ------- ------------------------------------- -------- ----------------
  Q-01    QC plan                                Fail     Not present in repository or artefacts made available to audit

  Q-02    QC checklist                           Fail     Not present in repository or artefacts made available to audit

  Q-03    QC findings documented and saved       Fail     Not present in repository or artefacts made available to audit
  -----------------------------------------------------------------------

## 7. Summary of Non-Conformances

  --------------------------------------------------------------------------
  NC ID          Phase          Checklist Item Status         Description
  -------------- -------------- -------------- -------------- --------------
  NC-01          Validating     V-01 ---       Pass           Undocumented
                                Requirements                  requirement
                                Change                        changes
                                Documentation                 confirmed via
                                                              NS-DECL-2026-001;
                                                              committed to
                                                              repository

  NC-02          Validating     V-02 ---       Partial        No documentary
                                Editorial                     evidence of
                                checks                        spell,
                                                              grammar, or
                                                              editorial
                                                              checks found
                                                              in repository

  NC-03          Validating     Q-01 ---       Fail           QC plan not
                 (QC team,      QC plan                       present in
                 §6)                                          repository or
                                                              artefacts made
                                                              available to
                                                              audit

  NC-04          Validating     Q-02 ---       Fail           QC checklist
                 (QC team,      QC checklist                  not present in
                 §6)                                          repository or
                                                              artefacts made
                                                              available to
                                                              audit

  NC-05          Validating     Q-03 ---       Fail           QC findings
                 (QC team,      QC findings                   not present in
                 §6)                                          repository or
                                                              artefacts made
                                                              available to
                                                              audit
  --------------------------------------------------------------------------

## 8. Conclusion

The Analysing and Specifying phases of the Nevon Solutions RE process
for Project P2-1561W are complete and well-evidenced. All seven
Analysing phase items and all four Specifying phase items were confirmed
as passing based on documentary evidence in the repository. Key
strengths include the thorough and systematic use of the IRC
(NS-IRC-2026-001), clear traceability of models from original to revised
versions, and the presence of all required standalone artefacts (IRC,
iRTM, Change Request Form Template, IEEE SRS template).

The Validating phase presents two areas that could not be confirmed from
Nevon's own artefacts. One item (NC-02) requires further investigation
to determine its status: evidence of editorial checks requires either
direct document access or interview/focus group confirmation. NC-01
(customer sign-off) has been resolved via the BioSec Change Request
Declaration Form (NS-DECL-2026-001) committed to the repository.

Three definitive non-conformances (NC-03, NC-04, NC-05) are
attributable to the external QC team: the QC plan, checklist, and
findings are absent from all artefacts reviewed. These are reported
separately in §7.

This report is a factual record of the process state as observed by
Paragon Assurance. No solutions or corrective actions are proposed.

## Annexes

*Annexes contain physical copies of standalone external artefacts
referenced as evidence in this report. To be populated as evidence is
gathered, particularly for items requiring follow-up (NC-02).*

  -----------------------------------------------------------------------
  Annex                               Description
  ----------------------------------- -----------------------------------
  Annex 1                             IRC --- Incongruous Requirements
                                      Checklist (NS-IRC-2026-001) ---
                                      evidence for A-06, A-07

  Annex 2                             Analysing Report cover page and
                                      sign-off --- evidence for A-01,
                                      A-02

  Annex 3                             SRS Section 1.2 (template
                                      reference) --- evidence for S-01

  Annex 4                             SRS Section 1.1 and iRTM reference
                                      --- evidence for S-02, S-03

  Annex 5                             BioSec Change Request Declaration
                                      Form (NS-DECL-2026-001) ---
                                      evidence for NC-01

  Annex 6                             *(To be added)* Interview/focus
                                      group record --- pending NC-02
                                      follow-up
  -----------------------------------------------------------------------

## Appendices

*Appendices contain detailed investigation notes where the search for
evidence was extended or non-trivial.*

  -----------------------------------------------------------------------
  Appendix                            Description
  ----------------------------------- -----------------------------------
  Appendix A                          Investigation notes ---
                                      Requirements change documentation
                                      (NC-01): undocumented quantitative
                                      thresholds and open issue
                                      resolutions identified during
                                      traceability review; basis for
                                      initial Partial status

  Appendix B                          Investigation notes --- QC
                                      artefacts (NC-03, NC-04, NC-05):
                                      repository search record,
                                      directories examined, null result
  -----------------------------------------------------------------------

*Report prepared by Paragon Assurance.*

  --------------------------------------------------------------------------------------
  Name                    Signature                              Date
  ----------------------- -------------------------------------- -----------------------
  *(Paragon Assurance     \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_   18 March 2026
  Representative)*

  --------------------------------------------------------------------------------------
