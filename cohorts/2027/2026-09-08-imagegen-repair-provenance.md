# Imagegen repair provenance — 2026-09-08

This ledger records the five screenshot repairs published in the focused
commit for the 2027 data warehouse and batch lessons. Each output was
generated with the built-in imagegen tool from the original non-crisp JPG and
the corresponding bounded crop. Existing crisp targets were used only as
layout/composition references where noted; no enlarged or sharpened derivative
was used as the source of truth.

Native output and a proportional 800px lesson-size render were inspected
before publication. Original JPGs and bounded crops remain preserved.

| Published target | Original source | Bounded crop | Imagegen output | Validation |
|---|---|---|---|---|
| `cohorts/2027/03-data-warehouse/images/01-data-warehouse-and-bigquery-06-partition-pruning-crisp.png` | `01-data-warehouse-and-bigquery-06-partition-pruning.jpg` | `01-data-warehouse-and-bigquery-06-partition-pruning-cropped.png` | `exec-673d2ac2-db5d-470e-93e5-c0da8abb769f.png` | Blue SQL selection removed; exact query/results composition retained; native and 800px checks passed. |
| `cohorts/2027/03-data-warehouse/images/01-data-warehouse-and-bigquery-08-cluster-pruning-crisp.png` | `01-data-warehouse-and-bigquery-08-cluster-pruning.jpg` | `01-data-warehouse-and-bigquery-08-cluster-pruning-cropped.png` | `exec-f8570e46-a73f-476b-a948-925bc1f709d0.png` | Blue SQL selection removed; dates, table names, counts, and result row retained; native and 800px checks passed. |
| `cohorts/2027/03-data-warehouse/images/06-deploying-a-machine-learning-model-03-docker-running-crisp.png` | `06-deploying-a-machine-learning-model-03-docker-running.jpg` | `06-deploying-a-machine-learning-model-03-docker-running-cropped.png` | `exec-d0e3136f-450f-4011-8ca9-feeafb84e125.png` | Tight terminal redraw keeps the exact `docker ps` row, ports, and `great_crazy` name; native and 800px checks passed. |
| `cohorts/2027/06-batch/images/05-spark-dataframes-03-built-in-functions-crisp.png` | `05-spark-dataframes-03-built-in-functions.jpg` | `05-spark-dataframes-03-built-in-functions-cropped.png` | `exec-04676e4d-c051-4dfd-9933-7425d3fc6c78.png` | Green active-cell border and webcam/browser artifacts removed; autocomplete and output retained; native and 800px checks passed. |
| `cohorts/2027/06-batch/images/11-operations-on-spark-rdds-06-dag-two-stages-crisp.png` | `11-operations-on-spark-rdds-06-dag-two-stages.jpg` | `11-operations-on-spark-rdds-06-dag-two-stages-cropped.png` | `exec-9b893bf0-b432-44ab-b10a-7b03ab9d8d94.png` | Connector visibly starts at the Stage 30 output node and reaches Stage 31 `partitionBy` with complete margins; native and 800px checks passed. |

The imagegen outputs are stored in the local generated-image directory under
`/home/alexey/.codex/generated_images/01a08261-323e-7721-9a78-009063449c6c/`.

## Published hashes

These hashes make the selected imagegen output auditable after copying it into
the lesson image paths.

| File | SHA-256 |
|---|---|
| `01-data-warehouse-and-bigquery-06-partition-pruning-crisp.png` | `3069ee3763028ad1945d423326d8829c9267b557f3125a1e327db2b3865ec245` |
| `01-data-warehouse-and-bigquery-08-cluster-pruning-crisp.png` | `5a87b8362f5234d3dcf9120ad8f66cd2bf3d248aa2ee81ea16dac8b22df836b5` |
| `06-deploying-a-machine-learning-model-03-docker-running-crisp.png` | `728cfc7d38e569e8db68b8621e501008605ee6261127a2decd1b042583888811` |
| `05-spark-dataframes-03-built-in-functions-crisp.png` | `4d719478c24cb4bce362ecf0ca54e0d162933924299a4991a6dd649e4b624d87` |
| `11-operations-on-spark-rdds-06-dag-two-stages-crisp.png` | `855afc5df9d8ca759534ec1297335e24973532a4fa5ac828043f1e6613655855` |

## Input hashes

| Repair | Original JPG SHA-256 | Bounded crop SHA-256 |
|---|---|---|
| Partition pruning | `11bcbf8c5cc5afb7945dba804c3bfbb78c8b2d90f6a0a2ca0a2a3c2ffaa3b875` | `7388943c58f6a1b3e56f747ad4c5d8615b1367958512af55873311e71e3d3c1c` |
| Cluster pruning | `9e30b6dfe4881a55f9188a144b5d0e50edc25e6e844d847c0aff8d2bb5046aec` | `60e175234f7690c56c33a1d5b586bd0ec4180a2f9edad15332a75b5b4faddd5d` |
| Docker running | `0b0266a6417fc628c06e317b42d4c114c0228667f913bcdf5837198910050998` | `0790349ec4b1994707d4faa3174028766adca031fdb541a08b91fa1577945360` |
| Spark built-in functions | `e446434b8e919d2e3ad53c34939e0cef2ff017fa6f8cb6fd9f3c4e0e422597e0` | `01b1a8bbce7f46b75a8405fd1b718e2d0ae35dcae5d25c4afb46a43c3068cdd2` |
| Spark RDD two-stage DAG | `a248d024dc20af56290836e8697ce8c7b3af950123323ea5012659b56666fabf` | `af5174e5a8e790ca18755d4c1e974e0e3b596b039a925c512d7c633f9c69b4ca` |
