# Frozen stability margin after resistive load shedding: data and code

Authors: Onur Ayvaz and Özgür Tomak. This repository accompanies a manuscript prepared for submission to *Sustainable Energy, Grids and Networks*.

`SEGAN_research_data_code_v1.zip` contains the computational model and test code, sealed member-level results from the internally fixed HDL2b run, and separate post-hoc prediction and local ODE outputs. It is a selected, readable research-data archive. The full fixed protocols and internal audit provenance are supplied to the journal as Supplementary Material S1.

To inspect the archived predictions, open `posthoc/posthoc_member_predictions.csv`. To reproduce the post-hoc analyses after extraction, install the packages in `requirements.txt` and run `python -I posthoc/reproduce_posthoc.py` and `python -I posthoc/reproduce_figure3.py` from the extracted archive root. The scripts use the retained model implementation and the sealed HDL2b CSV/JSON. They do not change the historical outputs.

The quadratic margin estimate is an empirical predictor for the tested model, not a certified operational shedding limit. The ODE traces perturb a post-shedding equilibrium locally; they do not simulate an abrupt shedding step. Original run-time software versions were not recorded; post-hoc versions are in `posthoc/posthoc_reproduction.json`.

The ZIP includes `SHA256SUMS`. A separate root-level `SHA256SUMS` identifies the downloaded ZIP. The study received no external funding. The authors declare no competing interests. License terms for this archive are in `LICENSE.md` inside the ZIP.
