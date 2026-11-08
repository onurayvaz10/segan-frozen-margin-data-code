# Frozen stability margin after resistive load shedding: data and code (archive v1.5)

Authors: Onur Ayvaz and Özgür Tomak. This archive accompanies a manuscript prepared for submission to *Sustainable
Energy, Grids and Networks*.

## Archive v1.5 (8 November 2026, current)

From v1.5 on, this repository carries the supplementary data/code archives **exactly as prepared for
submission with the manuscript**: the three files below are byte-identical to the supplementary ZIPs of the
submission package (SHA-256 values in `SHA256SUMS`).
Each contains its own read-only integrity check (Python standard library only).

| File | Content | Integrity check |
|---|---|---|
| `Supplementary_S1_Data_Code_2026-10-27.zip` | Supplementary Material S1: model and test code, fixed protocols, authorisation records, sealed outputs with hash lists, post-hoc analyses, revision cross-checks and the additions development_20261026, p92_20261026, figures_20261026 and p93_20261026 | `python -I verify_s1.py` in `S1_Data_Code/` (292 files; recomputes the primary counts) |
| `Supplementary_S3_Numerical_Validation_Data_Code.zip` | Supplementary Material S3: independent offline numerical models, native Virtual HIL captures (offline software validation; no CHIL/PHIL/laboratory evidence), corrected Y5 reanalysis, reproduction instructions (`REPRODUCE.txt`) | `python -I verify_s3.py` (323 files) |
| `Supplementary_S4_Additional_Analyses_Data_Code.zip` | Supplementary Material S4: timing benchmark of manuscript Table 9, the pre-registered port–reference, branch-tracking and decomposition analysis (S2 Appendix I.8) and the records of the Virtual HIL direction studies (S2 Appendix I.7); 38 large raw capture files are listed with their SHA-256 in `OMITTED_LARGE_FILES.csv` | `python -I verify_s4.py` (425 files) |

The protocol texts and records inside these archives are in Turkish, the working language of the project.

## Earlier files (kept for the record)

- `SEGAN_research_data_code_v1.zip`, `_v1.1.zip`, `_v1.2.zip`: selected public mirrors of v1.0–v1.2.
- `SEGAN_research_data_code_development_20261026.zip`, `SEGAN_research_data_code_p92_20261026.zip`: files of
  v1.3/v1.4. The authoritative versions of these additions are those inside the S1 archive above.
- `SEGAN_S1_Colab.ipynb`: Colab notebook of v1.1 for the v1.2 mirror.

## Quick start

    unzip Supplementary_S1_Data_Code_2026-10-27.zip -d s1 && cd s1/S1_Data_Code
    python -I verify_s1.py
    pip install -r requirements_pinned.txt   # Python 3.12, for the reproduction scripts

Reproduction instructions for each archive are in its own README/REPRODUCE file. Exact software-package versions of
the historical sealed runs were not recorded.

## Licence

Code under the MIT licence; data and documents under CC BY 4.0 (see `LICENSE` inside S1). `SHA256SUMS` lists every
archive file of this repository.
