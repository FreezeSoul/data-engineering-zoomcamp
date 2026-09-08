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

### 02-partitioning-vs-clustering-01-partitioning-options.jpg

- Source: `02-partitioning-vs-clustering.md`, partitioning options section.
- Rubric: 10/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 1, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the slide consolidates partitioning modes,
  time-unit choices, and the 4,000-partition limit in one reference.
- Preparation: deterministic crop `(x=20, y=20, width=600, height=300)`;
  resized 2x with a light unsharp mask. Exact wording and the documentation
  URL were retained.
- Method: deterministic PNG sibling
  `02-partitioning-vs-clustering-01-partitioning-options-cropped.png`.
- Invariants checked: all bullets, nested time intervals, `PARTITIONTIME`,
  the `4000` limit, and the source URL remain unchanged; no face, camera
  tile, cursor, or overlay was present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 02-partitioning-vs-clustering-02-clustering-basics.jpg

- Source: `02-partitioning-vs-clustering.md`, clustering basics section.
- Rubric: 10/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 1, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the slide summarizes column ordering, filter and
  aggregate-query benefits, the 1 GB caveat, and the four-column limit.
- Preparation: deterministic crop `(x=20, y=20, width=600, height=285)`;
  resized 2x with a light unsharp mask. Exact wording was retained.
- Method: deterministic PNG sibling
  `02-partitioning-vs-clustering-02-clustering-basics-cropped.png`.
- Invariants checked: all clustering bullets, nested query types, `< 1 GB`
  qualification, and the four-column limit remain unchanged; no face, camera
  tile, cursor, or overlay was present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 02-partitioning-vs-clustering-03-partitioning-vs-clustering.jpg

- Source: `02-partitioning-vs-clustering.md`, comparison table section.
- Rubric: 11/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 2, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the side-by-side table exposes trade-offs that
  are difficult to scan in prose, so it is retained with exact text.
- Preparation: deterministic crop `(x=20, y=20, width=600, height=300)`;
  resized 2x with a light unsharp mask. Imagegen was rejected because this
  is an exact comparison table.
- Method: deterministic PNG sibling
  `02-partitioning-vs-clustering-03-partitioning-vs-clustering-cropped.png`.
- Invariants checked: both headings, all four rows, and every cell value
  remain unchanged; no face, camera tile, cursor, or overlay was present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 02-partitioning-vs-clustering-04-clustering-over-partitioning.jpg

- Source: `02-partitioning-vs-clustering.md`, clustering-over-partitioning
  guidance.
- Rubric: 9/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 1, durability 2, caption/accessibility 1).
- Decision: `crop/replace`; the three concrete conditions are useful as a
  quick decision checklist even though the surrounding prose repeats them.
- Preparation: deterministic crop `(x=20, y=20, width=600, height=285)`;
  resized 2x with a light unsharp mask. Exact wording was retained.
- Method: deterministic PNG sibling
  `02-partitioning-vs-clustering-04-clustering-over-partitioning-cropped.png`.
- Invariants checked: all three conditions and the `1 GB` threshold remain
  unchanged; no face, camera tile, cursor, or overlay was present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 02-partitioning-vs-clustering-05-automatic-reclustering.jpg

- Source: `02-partitioning-vs-clustering.md`, automatic-reclustering section.
- Rubric: 10/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 1, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the slide explains why newly written blocks can
  weaken sort order and how background reclustering restores it.
- Preparation: deterministic crop `(x=20, y=20, width=600, height=300)`;
  resized 2x with a light unsharp mask. Exact wording was retained.
- Method: deterministic PNG sibling
  `02-partitioning-vs-clustering-05-automatic-reclustering-cropped.png`.
- Invariants checked: both explanatory paragraphs, all bullets, and the
  partition-scope qualification remain unchanged; no face, camera tile,
  cursor, or overlay was present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 03-bigquery-best-practices-01-cost-reduction.jpg

- Source: `03-bigquery-best-practices.md`, cost-reduction slide.
- Rubric: 10/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 1, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the checklist is a useful visual summary of
  concrete cost controls, while the original contains excess frame margin.
- Preparation: deterministic crop `(x=20, y=20, width=600, height=200)`;
  resized 2x with a light unsharp mask. Exact wording was retained.
- Method: deterministic PNG sibling
  `03-bigquery-best-practices-01-cost-reduction-cropped.png`.
- Invariants checked: `SELECT *`, query pricing, clustered/partitioned tables,
  streaming inserts, and staged materialization bullets remain unchanged; no
  face, camera tile, cursor, or overlay was present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 03-bigquery-best-practices-02-query-performance.jpg

- Source: `03-bigquery-best-practices.md`, query-performance slide.
- Rubric: 10/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 1, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the consolidated performance checklist adds a
  durable reference to the prose and code examples.
- Preparation: deterministic crop `(x=20, y=20, width=600, height=245)`;
  resized 2x with a light unsharp mask. Exact wording was retained.
- Method: deterministic PNG sibling
  `03-bigquery-best-practices-02-query-performance-cropped.png`.
- Invariants checked: all eight performance bullets, including JOIN, WITH,
  external-source, and oversharding guidance, remain unchanged; no face,
  camera tile, cursor, or overlay was present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 01-data-warehouse-and-bigquery-08-cluster-pruning.jpg

- Source: `01-data-warehouse-and-bigquery.md`, clustering query result.
- Rubric: 11/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 2, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the image supplies the query and measured
  `843.5 MB` result needed to compare with the `1.1 GB` estimate.
- Preparation: deterministic crop `(x=28, y=27, width=612, height=325)`;
  resized 2x with a light unsharp mask. Exact SQL and result values were
  retained rather than generated.
- Method: deterministic PNG sibling
  `01-data-warehouse-and-bigquery-08-cluster-pruning-cropped.png`.
- Invariants checked: clustered table selection, query text, bytes processed,
  and result row remain visible and unchanged; no face, camera tile, cursor,
  or unrelated browser chrome is present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 01-data-warehouse-and-bigquery-07-clustering-diagram.jpg

- Source: `01-data-warehouse-and-bigquery.md`, clustering section.
- Rubric: 11/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 2, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the diagram shows rows grouped by date and tag,
  which is a concrete relationship not conveyed as clearly by the prose.
- Preparation: deterministic crop `(x=20, y=18, width=600, height=335)`;
  resized 2x with a light unsharp mask. Imagegen was not used because the
  sample table values and highlighted ranges are exact evidence.
- Method: deterministic PNG sibling
  `01-data-warehouse-and-bigquery-07-clustering-diagram-cropped.png`.
- Invariants checked: source table, date-partitioned tables, tag grouping,
  highlighted ranges, table headings, and arrow direction remain unchanged;
  no face, camera tile, cursor, or overlay was present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 01-data-warehouse-and-bigquery-06-partition-pruning.jpg

- Source: `01-data-warehouse-and-bigquery.md`, partition-pruning query.
- Rubric: 11/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 2, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the query, highlighted date filter, and processed
  bytes provide execution evidence that prose alone does not show.
- Preparation: deterministic crop `(x=28, y=27, width=612, height=325)`;
  resized 2x with a light unsharp mask. Exact SQL and result metadata were
  retained rather than generated.
- Method: deterministic PNG sibling
  `01-data-warehouse-and-bigquery-06-partition-pruning-cropped.png`.
- Invariants checked: selected partitioned table, highlighted date range,
  query-result status, and the `105.9 MB` processed result remain visible;
  no face, camera tile, cursor, or unrelated browser chrome is present.
- Validation: output visually inspected; Markdown reference resolves and
  `git diff --check` passes.

### 01-data-warehouse-and-bigquery-05-partitioning-diagram.jpg

- Source: `01-data-warehouse-and-bigquery.md`, partitioning section.
- Rubric: 11/12 (instructional contribution 2, relevance 2, readability 1,
  complementarity 2, durability 2, caption/accessibility 2).
- Decision: `crop/replace`; the before/after table relationship teaches how
  `Creation_date` becomes date partitions, and exact sample rows must remain
  trustworthy.
- Preparation: deterministic crop `(x=20, y=18, width=600, height=335)`;
  resized 2x with a light unsharp mask. Imagegen was rejected for this
  table-heavy asset because it could alter exact rows or dates.
- Method: deterministic PNG sibling
  `01-data-warehouse-and-bigquery-05-partitioning-diagram-cropped.png`.
- Invariants checked: source and partitioned table headings, `Creation_date`,
  partition keys `20180301`, `20180302`, `20180303`, sample rows, and the
  partition arrow are unchanged; no face, camera tile, cursor, or overlay was
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
