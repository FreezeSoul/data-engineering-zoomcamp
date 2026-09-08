# DE 2027 batch image rollout

Scope: every local Markdown image reference under `cohorts/2027/06-batch/`.

Worker capability: `imagegen` skill available; built-in image generation used
only for bounded explanatory diagrams after deterministic crop and visual
inspection. Exact code, commands, URLs, plots, numeric output, and live UI
were handled with deterministic crops/upscales. Originals are preserved.

Rubric: each source was checked against the illustration rubric. A retained
image must have a specific teaching point, be relevant, readable, additive to
the nearby prose/code, durable enough for the lesson, and have a useful
caption. Images with no instructional contribution or redundant navigation
were removed. Temporary crops/contact sheets remain disposable under
`.tmp/de-batch-contact-sheets/` and are not course assets.

## Inventory and decisions

| # | Lesson/source | Decision | Method | Score | Teaching point / limitation |
|---:|---|---|---|---:|---|
| 1 | `01-introduction-to-batch-processing-01-batch-vs-streaming.jpg` | keep | imagegen from crop `x=37,y=0,w=465,h=340` | 10/12 | Cleaned diagram preserves the batch calendar → job → output and continuous streaming flow; removed presenter, webcam tile, toolbar, and borders. |
| 2 | `01-introduction-to-batch-processing-02-streaming-example.jpg` | keep | imagegen from crop `x=37,y=0,w=465,h=340` | 10/12 | Clean event-stream diagram preserves `RIDE.STARTS` → processor → output flow; removed presenter, webcam tile, toolbar, and borders. |
| 3 | `01-introduction-to-batch-processing-03-batch-job-frequencies.jpg` | keep | imagegen from crop `x=37,y=0,w=465,h=340` | 9/12 | Crisp list preserves the three schedule frequencies in order; removed presenter, webcam tile, toolbar, and borders. |
| 4 | `01-introduction-to-batch-processing-04-technologies.jpg` | keep | imagegen from crop `x=37,y=0,w=465,h=340` | 10/12 | Two-column diagram preserves batch frequencies and the Python/SQL/Spark/Flink technology list; removed recording artifacts. |
| 5 | `01-introduction-to-batch-processing-05-batch-workflow.jpg` | remove | — | 2/12 | Hard-gate failure: the source is an advantages list, not the workflow described by the surrounding text; it is also redundant with the adjacent advantages image. Original preserved. |
| 6 | `01-introduction-to-batch-processing-06-advantages.jpg` | keep | imagegen from crop `x=37,y=0,w=465,h=340` | 10/12 | Clean comparison preserves the three advantages and the delay disadvantage; removed recording artifacts. |
| 7 | `01-introduction-to-batch-processing-07-batch-vs-streaming-share.jpg` | keep | imagegen from crop `x=37,y=0,w=465,h=340` | 10/12 | Clean diagram preserves the approximate 80% batch / 20% streaming split and processing relationship; removed recording artifacts. |
| 8 | `02-introduction-to-spark-01-spark-google-search.jpg` | remove | — | 4/12 | Navigational Google results add no understanding beyond the surrounding definition of Spark, are transient, and are not complementary evidence. Original preserved. |
| 9 | `02-introduction-to-spark-02-data-processing-engine-whiteboard.jpg` | keep | imagegen from crop `x=37,y=0,w=465,h=340` | 10/12 | Clean cluster diagram preserves input data → Spark cluster → output data and the language note; removed presenter and recording UI. |
| 10 | `02-introduction-to-spark-03-when-to-use-spark-whiteboard.jpg` | keep | imagegen from crop `x=37,y=0,w=465,h=340` | 11/12 | Clean decision diagram preserves the SQL-versus-Spark recommendation and Hive/Presto/Athena labels; removed recording artifacts. |
| 11 | `02-introduction-to-spark-04-typical-workflow-whiteboard.jpg` | keep | imagegen from crop `x=37,y=0,w=465,h=340` | 11/12 | Clean workflow preserves SQL preparation, Spark/Python training, model creation, and Spark model application; removed recording artifacts. |
| 12 | `03-installing-spark-01-install-guide-java.jpg` | keep | deterministic crop `x=20,y=205,w=465,h=145`, 2x Lanczos/sharpen | 9/12 | Keeps the relevant Linux/Java/OpenJDK instructions, removes browser chrome and webcam, and intentionally excludes unrelated page/sidebar content. |
| 13 | `03-installing-spark-02-java-home.jpg` | keep | deterministic crop `x=20,y=32,w=480,h=300`, 2x Lanczos/sharpen | 10/12 | Preserves the exact extraction output, path, and `JAVA_HOME` command while removing browser chrome and webcam. |
| 14 | `03-installing-spark-03-spark-download-page.jpg` | keep | deterministic crop `x=0,y=28,w=490,h=305`, 2x Lanczos/sharpen | 9/12 | Preserves the exact Spark version and Hadoop build selectors, removes browser chrome/webcam, and focuses the relevant left content. |
| 15 | `03-installing-spark-04-spark-home.jpg` | keep | deterministic crop `x=20,y=32,w=480,h=300`, 2x Lanczos/sharpen | 10/12 | Preserves the exact unpack/remove/export commands and paths while removing browser chrome and webcam. |
| 16 | `03-installing-spark-05-spark-shell.jpg` | keep | deterministic crop `x=20,y=32,w=480,h=300`, 2x Lanczos/sharpen | 10/12 | Preserves the exact Spark 3.0.3 shell output and result `[1, 2, 3, 4, 5, 6, 7, 8, 9]` while removing browser chrome and webcam. |
| 17 | `04-first-look-at-spark-01-spark-ui.jpg` | keep | deterministic crop `x=0,y=28,w=480,h=320`, 2x Lanczos/sharpen | 9/12 | Preserves the Spark 3.0.3 Jobs UI and job-state evidence while removing browser tabs/chrome and webcam. |
| 18 | `04-first-look-at-spark-02-schema-problem-pandas.jpg` | keep | deterministic crop `x=22,y=30,w=465,h=300`, 2x Lanczos/sharpen | 10/12 | Preserves the exact `StringType` schema and pandas sample setup while removing browser chrome and webcam. |
| 19 | `04-first-look-at-spark-03-schema-structtype.jpg` | keep | deterministic crop `x=45,y=28,w=455,h=300`, 2x Lanczos/sharpen | 10/12 | Preserves the exact StructField declarations while removing editor chrome, webcam, and unrelated panels. |
| 20 | `04-first-look-at-spark-04-partitions-slides.jpg` | keep | imagegen from crop `x=132,y=50,w=350,h=270` | 10/12 | Clean diagram preserves cloud-storage partitions and Spark-cluster executor relationship; removed Slides chrome, selection handles, and presenter. |
| 21 | `04-first-look-at-spark-05-repartition-write-parquet.jpg` | keep | deterministic crop `x=22,y=30,w=465,h=300`, 2x Lanczos/sharpen | 10/12 | Preserves the exact schema, `repartition(24)`, and parquet write code while removing browser chrome and webcam. |
| 22 | `05-spark-dataframes-01-print-schema.jpg` | keep | deterministic crop `x=22,y=30,w=465,h=300`, 2x Lanczos/sharpen | 10/12 | Preserves the exact `printSchema()` output and typed columns while removing notebook chrome and webcam. |

## Validation

Validation will be completed after the last entry: all retained references
resolve, originals remain, `git diff --check` passes, and disposable
intermediates are not staged.
