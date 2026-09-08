# DE legacy/current image rollout

Scope: every local Markdown image reference in the assigned module directories
and cohort Markdown paths (`cohorts/2022`, `cohorts/2024`, `cohorts/2025`,
`cohorts/2026`, and `cohorts/2027/02-workflow-orchestration`).

The initial inventory contains 94 local references to 92 unique source paths.
The audit includes video thumbnails, exact Airflow/UI captures, explanatory
diagrams, workshop assets, and homework evidence. The 2022 IAM reference
originally used the wrong relative path; it is corrected to the existing
repository-root source in a focused commit.

Imagegen capability was available and the skill was read in full. Imagegen was
used only for the bounded incremental-loading decision tree after inspecting
the source and verifying every required label and branch. Exact UI, code,
URL, numeric, logo, and plot-like assets remain deterministic or unchanged.

## Accepted image changes

### Incremental-loading decision tree

- Source: `cohorts/2024/workshops/dlt_resources/incremental_loading.png`
- Reference: `cohorts/2024/workshops/dlt_resources/data_ingestion_workshop.md`
- Disposition: `crop/replace`, score 11/12. The tree teaches the choice among
  append, replace, and merge/upsert; the generated replacement preserves all
  labels, branch directions, and outcomes while making the typography and
  lines crisp.
- Method: built-in imagegen edit after local inspection; no face, camera tile,
  browser chrome, cursor, watermark, or extra component was present or added.
- Required invariants checked: `Is it stateful data?`, `NO`/`YES` branch order,
  `Can you request it incrementally?`, and the exact three dispositions.
- Replacement: `incremental_loading-imagegen.png`

### Homework dataset evidence

- Source: `02-workflow-orchestration/images/homework.png` (the identical
  original is also preserved in the 2025 and 2027 cohort image directories).
- References: the 2025, 2026, and 2027 workflow-orchestration homework files.
- Disposition: `crop/replace`, score 10/12. The screenshot uniquely shows the
  yellow and green 2021 assets that the assignment asks learners to ingest;
  it complements the written assignment with concrete filenames and sizes.
- Method: deterministic crop of each side after local inspection. Removed the
  browser address bars and reaction controls while preserving the exact
  filenames, sizes, dates, highlighted 2021 rows, and purple teaching notes.
- Crop: left pane `820x750+0+25`, right pane `820x760+824+25`, padded and
  appended to `1640x760`.
- Replacement: `02-workflow-orchestration/images/homework-cropped.png`
- No imagegen: exact UI text, filenames, dates, and numeric sizes are the
  source of truth.

### 2022 IAM search screen

- Source: `images/aws/iam.png`
- Reference: `cohorts/2022/week_2_data_ingestion/transfer_service/README.md`
- Disposition: `keep`, score 8/12. The screenshot directly supports the
  instruction to search for IAM before creating an access key, and its exact
  AWS labels are readable. The original relative reference was broken and was
  corrected to `../../../../images/aws/iam.png`.
- Method: retained exact source; no imagegen because this is a live UI whose
  labels are the source of truth. The source contains no face or camera tile.

## Audit record

The remaining source-by-source dispositions and scores will be recorded here
before the final validation commit. Video thumbnails are intentionally audited
as navigation assets, not regenerated as lesson illustrations; their presenter
faces and play buttons are part of the thumbnail role. Clean explanatory
diagrams and exact technical screenshots are retained when they already meet
the rubric, with the reason and source dimensions recorded in the final audit.
