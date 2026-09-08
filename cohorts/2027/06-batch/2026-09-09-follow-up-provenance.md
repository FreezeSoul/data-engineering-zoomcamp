# 06-batch illustration follow-up provenance — 2026-09-09

This ledger records the strict follow-up repairs for the 06-batch
illustrations. Each imagegen repair uses the original non-crisp JPG as the
factual source and a bounded crop as the composition/detail reference. The
published output is inspected at native resolution and at a proportional
608px-wide lesson render before it is committed. Originals and crops remain
preserved.

## MapPartitions diagram

| Published target | Original JPG SHA-256 | Bounded crop SHA-256 | Published output SHA-256 | Imagegen output | Validation |
|---|---|---|---|---|---|
| `images/12-spark-rdd-mappartition-01-map-partitions-diagram-imagegen.png` | `7db8b45581bcdda460a273ef9f0f5ba5b128a8e9b44f323250169902cb3fb106` | `b4eacca11cc92bf35c464c7f98dce8924492f4284d01f8ff9a32a5d6b573c075` | `70f194fe755ec4450a9b9ce85944f770ce7522a79cf086b15b97ad5aa7bacbe8` | `/home/alexey/.codex/generated_images/01a08324-9092-7f41-b36b-4be7f604bada/exec-9ac431f6-bbc4-473f-9471-9ec224466957.png` | Native `1774×887` and `608×304` render inspected. Exact `RDD`, `Partition`, `mapPartitions`, and `1TB` labels are present; presenter, camera, toolbar, and handwritten artifacts are absent. C2PA metadata identifies `gpt-image`/OpenAI. |

## Dataproc submit-job form

| Published target | Original JPG SHA-256 | Bounded crop SHA-256 | Published output SHA-256 | Imagegen output | Validation |
|---|---|---|---|---|---|
| `images/15-setting-up-a-dataproc-cluster-02-submit-job-form-crisp.png` | `2dc190d5becb85faa1528065388e2f87300d7fb1f46c9de14d16fec17e037ef0` | `52cf74160fffddcf55108190f46dfd5e7f960f6c191b92137d3470a3a90d036f` | `97eb3f5fe08d8aaa50cd0b27d0a9afaa9aac8e1738b86bf7a0cb780ee17cfb45` | `/home/alexey/.codex/generated_images/01a0833c-854d-7862-b9ae-3f5b7eeed1f5/exec-291b2909-8bda-40ae-b273-12502a1f320f.png` | Native `1586×992` and proportional `608×380` render inspected. The redraw shows the complete caption-promised form context: `PySpark`, the exact main Python file, no dependencies/JARs, and all three exact 2021 bucket arguments. Camera, browser chrome, cursor, selection, and overlays are absent; C2PA metadata identifies `gpt-image`/OpenAI. |
