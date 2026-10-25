# VTC-AUDIT Reproducibility Package

Author: **Isaac(Rucheng) Li**

This reproducibility package contains the finalized reproducibility pipeline for the quantitative results reported in the paper. The pipeline was simplified after completion of the experiments to provide a cleaner and more compact release. We use Google Colab as a lightweight reproducible runtime, allowing the experiments to be inspected or rerun without a separate local environment setup.

## Setup and contents

Upload the full `VTC_AUDIT` folder to the root of Google Drive and keep the folder name exactly as:

```text
MyDrive/VTC_AUDIT/
```

The four notebooks are located in:

```text
MyDrive/VTC_AUDIT/codes/
```

- `01_VTC_AUDIT_Qwen3_5_9B.ipynb`
- `02_VTC_AUDIT_OneVision_2_8B.ipynb`
- `03_VTC_AUDIT_InternVL3_5_8B.ipynb`
- `04_VTC_AUDIT_Reproduce_Paper_Data.ipynb`

The first three notebooks run the finalized VTC-AUDIT experiments for the three VLMs on both seed 42 and seed 2026. The fourth notebook reads those outputs and reconstructs the paper tables and reported summary statistics. Since completed outputs are already included, run the fourth notebook directly to reproduce the tables without rerunning inference.

Consolidated run outputs are already included in:

```text
MyDrive/VTC_AUDIT/results/run/
```

with separate directories for `seed_42` and `seed_2026`.

To keep the reproducibility package compact, intermediate chunk-level inference checkpoints are not included. These files are used only for checkpointing and resuming inference and are regenerated automatically when the inference notebooks are rerun.

Paper-level tables, replication summaries, and verification outputs are included in:

```text
MyDrive/VTC_AUDIT/results/meta results/
```

The included consolidated outputs can be inspected directly and used by the fourth notebook to reconstruct the reported tables and summary statistics without rerunning model inference. The first three notebooks are provided for reproducing the inference pipeline when needed.

## Notes

For the public release, notebook execution outputs and transient widget metadata have been cleared. All code cells and the stored CSV, JSON, and Parquet experimental results are unchanged. The author is Isaac Li.

Because the released pipeline was simplified after the experiments, a small number of displayed table values may differ from the manuscript by at most ±0.01 due to floating-point and rounding conventions. These differences are limited to the final displayed values and do not affect the underlying results or conclusions.

To keep the release focused solely on reproducing the reported results, the package includes only the finalized experimental and analysis pipeline. We did not conduct a systematic compression-ratio sweep as part of the main study, so preliminary ratio-related experiments and other non-final exploratory materials are not included.