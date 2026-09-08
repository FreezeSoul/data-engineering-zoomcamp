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

### 01-data-warehouse-and-bigquery-01-olap-vs-oltp.jpg

- Source: `01-data-warehouse-and-bigquery.md`, OLTP/OLAP comparison section.
- Rubric: 11/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 2, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the table gives a compact comparison that is
  useful beyond the surrounding prose, but the source is soft and has excess
  frame margin.
- Preparation: deterministic crop `(x=20, y=10, width=600, height=340)`;
  resized 2x with a light unsharp mask. No exact text was regenerated.
- Method: deterministic PNG sibling
  `01-data-warehouse-and-bigquery-01-olap-vs-oltp-cropped.png`.
- Invariants checked: OLTP/OLAP headings, all four comparison rows, and every
  table value remain unchanged; no face, camera tile, cursor, or overlay was
  present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 01-data-warehouse-and-bigquery-04-external-table-details.jpg

- Source: `01-data-warehouse-and-bigquery.md`, external-table section.
- Rubric: 10/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 2, durability 1, caption/accessibility 2).
- Decision: `crop/replace`; the UI state proves the table is external and
  shows its zero-byte size, source URIs, and CSV format, but the original
  includes a thin capture frame and small text.
- Preparation: deterministic crop `(x=28, y=25, width=612, height=330)`;
  resized 2x with a light unsharp mask. The exact UI was not regenerated.
- Method: deterministic PNG sibling
  `01-data-warehouse-and-bigquery-04-external-table-details-cropped.png`.
- Invariants checked: Explorer context, table details, source URI rows,
  `0 B` size, `CSV` source format, and external-data heading remain visible;
  no face, camera tile, cursor, or unrelated browser chrome is present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 01-data-warehouse-and-bigquery-03-bigquery-cost.jpg

- Source: `01-data-warehouse-and-bigquery.md`, BigQuery pricing section.
- Rubric: 10/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 1, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the slide makes the on-demand/flat-rate cost
  distinction and the concrete `$5`, `100 slots`, `$2,000/month`, and `400 TB`
  figures scannable, while the original has unnecessary whitespace.
- Preparation: deterministic crop `(x=20, y=20, width=560, height=220)`;
  resized 2x with a light unsharp mask. Exact text and numbers were retained.
- Method: deterministic PNG sibling
  `01-data-warehouse-and-bigquery-03-bigquery-cost-cropped.png`.
- Invariants checked: pricing headings, bullets, slot count, dollar amounts,
  and data-volume statement are unchanged; no face, camera tile, cursor, or
  overlay was present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.
