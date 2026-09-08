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

## Spark master UI — no workers

| Published target | Original JPG SHA-256 | Bounded crop SHA-256 | Published output SHA-256 | Imagegen output | Validation |
|---|---|---|---|---|---|
| `images/14-creating-a-local-spark-cluster-01-spark-master-ui-crisp.png` | `acbe938fb541ae8322b9e3bcb9c64663a811a121914f3e071393b35dec38978d` | `58db735dd0302ad646017145809db8a50d3a8f9e9c890c9d7e342b513dd8761c` | `728d0410f1436eb3f7c26140d05de26afeba55dffc8eaa49935fa634143db77c` | `/home/alexey/.codex/generated_images/01a0833c-854d-7862-b9ae-3f5b7eeed1f5/exec-5c8cae56-3a93-4b1e-b0af-0798f84227b9.png` | Native `1672×941` and proportional `608×342` renders inspected. The redraw preserves Spark `3.0.3`, the master URL, `ALIVE` status, zero workers, zero applications, and the empty tables. Camera, browser chrome, cursor, selection, and overlays are absent; C2PA metadata identifies `gpt-image`/OpenAI. |

## Spark master UI — worker registered

| Published target | Original JPG SHA-256 | Bounded crop SHA-256 | Published output SHA-256 | Imagegen output | Validation |
|---|---|---|---|---|---|
| `images/14-creating-a-local-spark-cluster-02-worker-registered-crisp.png` | `ebbf95dd6eaf2196d9069f3360303004886952231b15e1edb6364c9fba97c106` | `3bbc5fa8eb6b078349a434752ef3625ba02c6da40d86e16178ef1f7df4a039d3` | `97b571bb5cf58e35e78f465417cc103207af1e212193f7c5d15260c98d8bd987` | `/home/alexey/.codex/generated_images/01a0833c-854d-7862-b9ae-3f5b7eeed1f5/exec-ceb6c26f-2f24-4692-b2f1-9538aabde78f.png` | Native `1672×941` and proportional `608×342` renders inspected. The redraw preserves one `ALIVE` worker, exact worker/address identifiers, resource values, one `RUNNING` application, and one `FINISHED` application. Camera, browser chrome, cursor, selection, and overlays are absent; C2PA metadata identifies `gpt-image`/OpenAI. |

## BigQuery connector traceback — removed

| Former published target | Original JPG SHA-256 | Bounded crop SHA-256 | Former output SHA-256 | Decision |
|---|---|---|---|---|
| `images/16-connecting-spark-to-bigquery-02-failed-to-find-bigquery-crisp.png` | `f5bd4950c6b57cad657d6e787b58c84aa7bd9688b52546d583625a4b46b3880b` | `65d7259a7c58b69a03982db395c85fcb4063aa6f63c10692d76708ed98265f44` | `dd7a40484fc34b5fc8e543b8ca81e20ef166745bf6c72e1de006b19c238fc927` | Removed the Markdown embed. This is exact traceback/code output and is more useful as native lesson text; retaining it as a bitmap adds no instructional value and preserves capture artifacts. The JPG, crop, and PNG remain in the repository for auditability. |
