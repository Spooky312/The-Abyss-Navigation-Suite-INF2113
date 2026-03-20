# AI Review Prompt — Domain B: Specifying Method

## Overview

You are reviewing a Requirements Engineering process against the Specifying Method domain. You will be provided with three documents:
- The **Software Requirements Specification (SRS)**
- The **Requirements Traceability Matrix (iRTM)** or equivalent traceability document
- The **Analysing Report** or equivalent analysis artefacts

Provide a **narrative report** identifying:
- Evidence of compliance with each checklist item within these three documents
- Missing sections, inconsistencies, or unresolved issues
- Specific document locations where evidence is (or should be) present
- Cross-document discrepancies (SRS vs. Analysing Report, SRS vs. iRTM)

---

## Checklist Items to Verify

**B.1** — Does the SRS reference a recognised template?
Look for: Title page or introduction in SRS acknowledging a standard template (IEEE 830, IEEE 29148, or similar).

**B.2** — Are all SRS requirements traceable to earlier analysis/repository requirements via a traceability matrix?
Look for: iRTM showing mappings between SRS requirements and analysis sources; check for any SRS requirements without source traceability; verify alignment between analysis artefacts and SRS.

**B.3** — Does the traceability matrix exist as a standalone, extractable document?
Look for: Standalone iRTM document; verify it is complete and independently usable.

**B.4** — Is terminology consistent across all SRS sections and the Analysing Report?
Look for: Data dictionary or glossary in SRS; verify terms are used consistently throughout SRS sections; cross-check terminology with the Analysing Report.

**B.5** — Were all open issues from the analysis phase resolved before SRS finalisation?
Look for: Analysing Report open issues section; verify that all noted issues are either closed or addressed in the SRS with documented resolution.

**B.6** — Were contradictory requirements identified and resolved before specifying?
Look for: Evidence in Analysing Report of conflict identification; verify that contradictions are resolved in the SRS without conflicts remaining.

**B.9** — Was the SRS submitted at a final version level (≥ Version 1.0)?
Look for: Cover page version number in SRS; flag if version is below 1.0 when marked as final.

---

## Guidance for Your Report

For each item, note:
1. **Status**: Is evidence present, partial, or missing?
2. **Location**: Section/document reference where evidence is found or expected
3. **Discrepancy**: Any gaps or inconsistencies across the three documents
4. **Cross-document alignment**: Flag any conflicts or misalignments between SRS, iRTM, and Analysing Report

Highlight:
- Unresolved open issues from analysis
- Broken traceability chains in iRTM
- Terminology inconsistencies between documents
- Contradictions not resolved before specifying
- Version control issues in SRS
