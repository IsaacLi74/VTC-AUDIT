# VTC-AUDIT

Code and experimental results for **VTC-AUDIT: An Interventional Reliability Audit for Visual-Token Compression under Paired Image Shifts**.

**Isaac(Rucheng) Li · University of Pittsburgh**  
[isl74@pitt.edu](mailto:isl74@pitt.edu)

## Reproduce the paper tables

1. Download and extract this repository (**Code → Download ZIP**).
2. Copy the inner `VTC_AUDIT` folder to Google Drive: `MyDrive/VTC_AUDIT/`.
3. Open [`04_VTC_AUDIT_Reproduce_Paper_Data.ipynb`](VTC_AUDIT/codes/04_VTC_AUDIT_Reproduce_Paper_Data.ipynb) in Google Colab and run all cells. The completed outputs are included; this step needs no model inference or GPU.

To rerun inference, use notebooks `01`–`03` with a suitable GPU runtime. See the [setup notes](VTC_AUDIT/README.md).

## Contents

- `VTC_AUDIT/codes/`: four notebooks.
- `VTC_AUDIT/results/run/`: six completed runs, using benchmark manifests 42 and 2026.
- `VTC_AUDIT/results/meta results/`: paper tables and verification summaries.

The audit covers three VLMs, DivPrune and ApET at 25% retained positions, and 708,000 inference records. Notebook execution outputs have been cleared; code and saved experimental results are preserved. Displayed values can differ by 0.01 because of rounding conventions.

Citation metadata: [`CITATION.cff`](CITATION.cff).
