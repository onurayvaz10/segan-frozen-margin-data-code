# Frozen stability margin after resistive load shedding: data and code (archive v1.1)

Authors: Onur Ayvaz and Özgür Tomak. This archive accompanies a manuscript prepared for submission to *Sustainable
Energy, Grids and Networks*. It is a selected public mirror of Supplementary Material S1: it contains the model and
test code, the sealed HDL2b member-level outputs with their hash list, the post-hoc analyses and the revision
cross-checks of 25 October 2026. The fixed protocol texts, the decision log and the internal audit records are part
of Supplementary Material S1 submitted to the journal.

**One-click reproduction on Google Colab:** open `colab/SEGAN_S1_Colab.ipynb` in Colab (*File ▸ Upload notebook*,
or *File ▸ Open notebook ▸ GitHub* with this repository), choose *Runtime ▸ Run all* and upload the archive zip when
asked. The notebook checks the hash lists, builds an isolated Python 3.12 environment with the pinned versions, runs
every script below on a working copy, compares the regenerated numbers with the distributed files and shows the
report and Figures 1–8 (about 4–5 minutes). On any other computer: `python colab/run_all.py --root . --python <python>`.
See `colab/README_COLAB.md`.

Reproduce step by step (Python 3.12; `pip install -r requirements_pinned.txt`), from the archive root:

    python -I posthoc/reproduce_tables.py
    python -I posthoc/reproduce_posthoc.py
    python -I posthoc/reproduce_figure3.py
    python -I posthoc/abrupt_validation.py
    python -I posthoc_revision_20261025/stats_audit.py . posthoc_revision_20261025/stats_audit.json
    python -I posthoc_revision_20261025/math_check.py posthoc_revision_20261025/math_check.json
    python -I posthoc_revision_20261025/abrupt_shedding_window.py 3.0
    python -I posthoc_revision_20261025/solver_check.py
    python -I posthoc_revision_20261025/make_figures.py

The pin check `python -I research_intelligence/cdl1/code/hdl2b_run.py --check-only` needs the fixed protocol and
audit records that are only in Supplementary Material S1; it is therefore not part of this mirror.

Changes from v1.0: the English-named aliases and the hash list of the sealed HDL2b output are included (the v1.0
mirror lacked them, and the current post-hoc scripts read the English names); the post-hoc scripts are the versions
submitted with S1; the abrupt-shedding scripts and the revision folder are added. Note: over a 3 s window the
abrupt-shedding cases at the quadratic estimate and at the recorded reference diverge; only the frozen case converges.
The quadratic margin estimate is an empirical predictor for the tested model, not a shedding limit.
`posthoc_revision_20261025/math_check.py` selects the eigenvalue branch of the Lemma 1 toy check by its real part
(second pass of 25 October 2026); the previous selection depended on the eigenvalue order of the numpy version.

Licence terms are in `LICENSE.md`. `SHA256SUMS` lists every file of this archive.

