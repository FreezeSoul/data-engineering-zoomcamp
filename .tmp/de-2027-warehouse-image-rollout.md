# Data Warehouse 2027 image rollout

Scope: every local Markdown image reference under
`cohorts/2027/03-data-warehouse/`. The inventory contains 33 source
references across six lessons. Originals are preserved beside any new
asset. Each accepted replacement or removal is committed separately.

The imagegen capability was available for this worker. Bounded explanatory
diagrams were eligible for imagegen after deterministic crop and local
inspection. Exact code, commands, URLs, plots, numeric/table output, and
live UI use deterministic crops or exports instead. No source in this
scope contains a webcam face or camera tile; BigQuery, terminal, and
Postman chrome is removed only where it is outside the instructional UI.

## Disposition record

### 01-data-warehouse-and-bigquery-02-data-warehouse-diagram.jpg

- Source: `01-data-warehouse-and-bigquery.md`, architecture paragraph.
- Rubric: 11/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 2, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the architecture is essential, but the 640px
  source was soft at lesson size.
- Preparation: deterministic crop `(x=20, y=15, width=560, height=300)`;
  the crop removed empty frame margins and was sent as the imagegen
  reference.
- Method: built-in imagegen, `scientific-educational`; generated sibling
  `01-data-warehouse-and-bigquery-02-data-warehouse-diagram-imagegen.png`.
- Invariants checked: the title, two bullets, source/staging/warehouse/data
  mart/user stages, operational systems, flat files, metadata, summary data,
  raw data, purchasing, sales, inventory, analysis, reporting, mining, and
  left-to-right relationships are retained; no people, controls, browser
  chrome, cursor, watermark, or extra component appears.
- Validation: output visually inspected at 1680px wide; Markdown reference
  resolves and `git diff --check` passes.
