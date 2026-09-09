# 06-batch illustration follow-up provenance — 2026-09-09

This ledger records the strict follow-up repairs for the 06-batch
illustrations. Each imagegen repair uses the original non-crisp JPG as the
factual source and a bounded crop as the composition/detail reference. The
published output is inspected at native resolution and at a proportional
608px-wide lesson render before it is committed. Originals and crops remain
preserved. The crop coordinates below are measured in the original `640×360`
frame; the tracked crop hash is the authoritative byte-level reference.

## Strict 06-batch semantic repairs

These four outputs repair the semantic defects found by the strict 06-batch
review. Each was generated with the original non-crisp JPG and a fresh,
native-resolution bounded crop as imagegen inputs. The generated artifact was
copied byte-for-byte into the published target; no resize, sharpening, or
post-generation text edit was used. C2PA identifiers were read from the
published PNGs.

| Published target | Original JPG SHA-256 | Fresh crop (geometry; SHA-256) | Imagegen artifact | Published output SHA-256 | C2PA / validation |
|---|---|---|---|---|---|
| `images/04-first-look-at-spark-01-spark-ui-crisp.png` | `59ab4b83b501e10b8e70ee48ee560282ba1c47fc566563d64ae9fa2c3ce67f8a` | `x=0,y=27,w=640,h=213`; `f61658745eaf6c73f6ba4a458ba074f5944a6c4a011df2a5dd85f66afaab82ad` | `/home/alexey/.codex/generated_images/01a083f5-2669-7b33-9eee-fc91bf35902a/exec-2deec469-6837-46af-87aa-1d51980902d6.png` | `af09ca8730dcd3e2864f80f7cece625bc6406630643ba40ee6f9e16f9f2208ec` | `urn:c2pa:1375db67-a8d4-43fe-a0e3-79ac6c737bac`; native `2170×725` and 608px `608×203` inspected. Blank Jobs page is preserved; the lesson wording now describes the application Jobs page rather than claiming a visible job row. |
| `images/04-first-look-at-spark-02-schema-problem-pandas-crisp.png` | `53d58e89d35b4ffc5e0462d80728e734bb37d08f49df3bfdabcbac3804ecb704` | `x=0,y=27,w=600,h=215`; `dba05af6d0c2d0dcfd9f0b754f32f181c14e8c67213ea82927ae99a503e09e87` | `/home/alexey/.codex/generated_images/01a083f5-2669-7b33-9eee-fc91bf35902a/exec-7e027aba-fe1d-4717-ae69-1e58bca5bbbe.png` | `540cb55a9a4308c87707fbfb0bc3f62fd7cd47110d6f4494e3d1006e4a3e495a` | `urn:c2pa:9f042254-5254-43d8-b1a2-6e7aa4ea83c6`; native `2098×750` and 608px `608×217` inspected. The command visibly uses exact `head -n 101`, not `1001`. |
| `images/04-first-look-at-spark-04-partitions-slides-imagegen.png` | `33be12471c94b2b6f7001915b11bc0c510f1cb02e35c6ddf4d0f9ed4f0c144a2` | `x=131,y=20,w=467,h=220`; `819b09469da6be9a708be81a0e22d80742a68e836a9ba35beba54462f3c6cb11` | `/home/alexey/.codex/generated_images/01a083f5-2669-7b33-9eee-fc91bf35902a/exec-14476e43-1941-48c3-a072-b3fa37331edb.png` | `d8699e24408e321ac126a08e72cd1f6eb105664665df2e60d69347ef1bd4cdf9` | `urn:c2pa:2093003d-efe6-4f04-9901-95f03e97c023`; native `1672×941` and 608px `608×342` inspected. Six arrows terminate inside matching `Executor 1`–`Executor 6` boxes. An earlier generated grid variant was rejected because three arrows landed between boxes. |
| `images/05-spark-dataframes-03-built-in-functions-crisp.png` | `e446434b8e919d2e3ad53c34939e0cef2ff017fa6f8cb6fd9f3c4e0e422597e0` | `x=0,y=27,w=600,h=215`; `2da9f4e8080cac06a509cbf964d72d9c1375b779e4944f28b144e406d0d2767e` | `/home/alexey/.codex/generated_images/01a083f5-2669-7b33-9eee-fc91bf35902a/exec-e15f8c91-2fdc-4a5e-a333-80c30317d281.png` | `301d8a17b22b44b536de506ca1fb1beda8519ecb491a5348154222c1ba0fb29e` | `urn:c2pa:99f899e3-6162-4916-ad5c-0e1291c63e5a`; native `1672×941` and 608px `608×342` inspected. The SQL context and DataFrame filter both show the exact quoted value `'HV0003'`. |

The four bounded crops above were created with ImageMagick 6.9.12-98 using
the native original frames:

```bash
convert <original.jpg> -crop <width>x<height>+<x>+<y> +repage -strip \
  -define png:exclude-chunk=tIME <target-imagegen-crop.png>
```

The four 608px validation renders are reproducible with
`convert <published.png> -resize '608x608>' <validation.png>` and are kept
outside the repository under `/tmp/de-batch-06-batch-repair-608/`.

## Typical Spark workflow — MODEL application-flow repair

The strict review found that the previous redraw showed `MODEL` beside
`SPARK APPLY ML` but did not connect them. The output was regenerated from the
original non-crisp video frame and a fresh native-resolution crop. The new
diagram makes the required directed `MODEL` → `SPARK APPLY ML` relationship
explicit while preserving the lesson's SQL preparation, Spark/Python training,
and data-lake flow. The presenter, webcam inset, editor controls, and other
capture artifacts are removed.

| Published target | Original JPG SHA-256 | Native bounded crop (geometry; SHA-256) | Imagegen artifact (SHA-256) | Published output SHA-256 | C2PA / validation |
|---|---|---|---|---|---|
| `images/02-introduction-to-spark-04-typical-workflow-whiteboard-imagegen.png` | `28d74acb2c1a4787aeb2bef9126292a8089e32981e45b8d1495ed6bd786161c1` | `x=54,y=3,w=528,h=330`; `ff32c3ac3264b74e8029173dd38d4da95614ad3a32f14edb7221024dc716f7e3` | `/home/alexey/.codex/generated_images/01a0846a-ff62-7b53-ab57-4f77fb0a4f0e/exec-a37f9f13-3d22-4560-892b-fc44d8bebb15.png`; `552a80c8b4ccf18555a756ca9c818c9c976c456da5863932b5383bbeb1423d95` | `552a80c8b4ccf18555a756ca9c818c9c976c456da5863932b5383bbeb1423d95` | `urn:c2pa:13a81cf3-3e5e-4450-8e26-d0e7c0867a74`; native `1942×809` and proportional 608px `608×253` inspected. The output is byte-identical to the imagegen artifact; the directed MODEL-to-SPARK APPLY ML arrow, exact labels, and no-face/no-overlay constraints were checked at both sizes. |

The crop was created from the native `640×360` JPG without scaling or
sharpening:

```bash
convert 02-introduction-to-spark-04-typical-workflow-whiteboard.jpg \
  -crop 528x330+54+3 +repage -strip -define png:exclude-chunk=tIME \
  02-introduction-to-spark-04-typical-workflow-whiteboard-imagegen-crop.png
```

The imagegen prompt required these exact labels: `RAW DATA`, `LAKE`,
`SQL / ATHENA`, `SPARK`, `PYTHON TRAIN ML`, `MODEL`, `SPARK APPLY ML`, and
`LAKE`. It explicitly required the SQL → Spark/Python training → MODEL →
SPARK APPLY ML flow and prohibited invented text, faces, camera/browser UI,
watermarks, overlays, and simple enlargement/sharpening. The generated PNG
was copied byte-for-byte into the published target with no post-generation
resize, sharpening, or text edit.

## MapPartitions diagram

| Published target | Original JPG SHA-256 | Bounded crop SHA-256 | Published output SHA-256 | Imagegen output | Validation |
|---|---|---|---|---|---|
| `images/12-spark-rdd-mappartition-01-map-partitions-diagram-imagegen.png` | `7db8b45581bcdda460a273ef9f0f5ba5b128a8e9b44f323250169902cb3fb106` | `b4eacca11cc92bf35c464c7f98dce8924492f4284d01f8ff9a32a5d6b573c075` | `70f194fe755ec4450a9b9ce85944f770ce7522a79cf086b15b97ad5aa7bacbe8` | `/home/alexey/.codex/generated_images/01a08324-9092-7f41-b36b-4be7f604bada/exec-9ac431f6-bbc4-473f-9471-9ec224466957.png` | Native `1774×887` and `608×304` render inspected. Exact `RDD`, `Partition`, `mapPartitions`, and `1TB` labels are present; presenter, camera, toolbar, and handwritten artifacts are absent. C2PA metadata identifies `gpt-image`/OpenAI. |

The exact bounded crop is retained at
`images/12-spark-rdd-mappartition-01-map-partitions-diagram-cropped.png`.
It is the `465×340` region `x=37,y=0,w=465,h=340`, extracted from the
original `640×360` JPG before the imagegen repair.

## Dataproc create-cluster form

| Published target | Original JPG SHA-256 | Fresh bounded crop SHA-256 | Imagegen artifact SHA-256 | Published output SHA-256 | Validation |
|---|---|---|---|---|---|
| `images/15-setting-up-a-dataproc-cluster-01-create-cluster-crisp.png` | `bcbc1727edf57f8792b975af2b6206c7058928299c32873ad04069ce04092876` | `7cca0e94be7edacb547c04f974188958589905f26e3c7e09bf655c21c6c96ef1` | `cd7e76b3b1c8bf24bd9cf3cecfbadb66b79e26942e4bbc63c88fbf9e9d50863f` | `cd7e76b3b1c8bf24bd9cf3cecfbadb66b79e26942e4bbc63c88fbf9e9d50863f` | Fresh imagegen redraw copied byte-for-byte into the published target. Native `1598×984` and proportional `608×374` renders inspected; exact Dataproc setup labels and selected Jupyter/Docker components are preserved. The output contains `gpt-image`/OpenAI C2PA metadata and has no webcam, browser chrome, cursor, or overlay artifacts. |

The new imagegen input crop is retained at
`images/15-setting-up-a-dataproc-cluster-01-create-cluster-imagegen-crop.png`.
It is a native-resolution `535×330` crop at `x=0,y=30,w=535,h=330` from the
original `640×360` JPG. It is intentionally not upscaled or sharpened before
imagegen. The exact crop command, including the tool version used, is:

```bash
# ImageMagick 6.9.12-98 Q16 x86_64 18038
convert 15-setting-up-a-dataproc-cluster-01-create-cluster.jpg \
  -crop 535x330+0+30 +repage -strip -define png:exclude-chunk=tIME \
  15-setting-up-a-dataproc-cluster-01-create-cluster-imagegen-crop.png
```

The resulting crop is SHA-256
`7cca0e94be7edacb547c04f974188958589905f26e3c7e09bf655c21c6c96ef1`.
The imagegen artifact was generated from both the original JPG and this fresh
crop. It was saved at
`/home/alexey/.codex/generated_images/01a0836e-71b4-7e51-81c7-c5b905ca6493/exec-64b34174-22aa-4a10-b641-ab7c83a96f31.png`, has SHA-256
`cd7e76b3b1c8bf24bd9cf3cecfbadb66b79e26942e4bbc63c88fbf9e9d50863f`, and was
copied without post-processing to the published target. The published target
therefore has the identical SHA-256 and retains the imagegen C2PA metadata.

The exact imagegen prompt was:

```text
Use case: ui-mockup
Asset type: high-resolution instructional lesson illustration
Primary request: Recreate the Google Cloud Dataproc “Create a cluster” setup form as a clean, crisp, high-resolution raster illustration. Use Image 1 (the original non-crisp video frame) and Image 2 (the freshly bounded native-resolution crop) only as factual/layout references. Redraw the visible interface cleanly; do not upscale or sharpen the screenshot.
Input images: Image 1: original non-crisp JPG, factual source; Image 2: freshly bounded crop, composition/detail reference.
Scene/backdrop: clean white Google Cloud console interface with a blue cloud-console header and a narrow left navigation rail.
Subject: the “Create a cluster” page. Keep the left setup navigation and the right “Optional components” checklist.
Style/medium: faithful typeset UI redraw, precise vector-like edges, high-resolution bitmap output, neutral white background.
Composition/framing: wide landscape composition matching the reference; show the complete relevant form area, including the “Create a cluster” heading, left setup steps, right optional-components checklist, and Create/Cancel controls.
Text (verbatim): “Google Cloud Platform”, “de-zoomcamp-nytaxi”, “Search”, “dataproc”, “Create a cluster”, “Set up cluster”, “Begin by providing basic information.”, “Configure nodes (optional)”, “Change node compute and storage capabilities.”, “Customize cluster (optional)”, “Add cluster properties, features, and actions.”, “Manage security (optional)”, “Change access, encryption, and security settings.”, “Optional components”, “Select one or multiple components.”, “Learn more”, “Anaconda”, “Hive WebHCAT”, “Jupyter Notebook”, “Zeppelin Notebook”, “Druid”, “Presto”, “ZooKeeper”, “Ranger”, “HBase”, “Flink”, “Docker”, “Solr”, “CREATE”, “CANCEL”.
Constraints: preserve the factual layout and exact labels from the references; Jupyter Notebook and Docker are checked; all other optional components are unchecked; keep the selected project text “de-zoomcamp-nytaxi”; retain the blue header and console navigation as clean UI context.
Avoid: the presenter’s face, webcam circle, browser tabs/address bar, browser chrome, cursor, annotations, handwritten marks, selection highlights, watermarks, invented fields, altered labels, extra components, illegible text, cropped checklist rows, and any screenshot-like blur or simple enlargement.
```

The prior `images/15-setting-up-a-dataproc-cluster-01-create-cluster-cropped.png`
is retained as historical audit evidence for the superseded output. Its
`1070×660` bytes were produced by an undocumented 2× Lanczos/sharpen step and
could not be reproduced (`AE=265712`, `MAE=710.214`); it is not an input to
the new imagegen chain and is no longer used to substantiate the published
output.

For the required display check, resize the published output without sharpening:

```bash
convert 15-setting-up-a-dataproc-cluster-01-create-cluster-crisp.png \
  -resize '608x608>' /tmp/dataproc-create-cluster-608.png
```

Expected render dimensions are `608×374`; inspect both the native target and
that render for readable labels, complete checklist rows, and absence of
camera/browser/overlay artifacts.

## Dataproc reports in bucket

| Published target | Original JPG SHA-256 | Bounded crop SHA-256 | Published output SHA-256 | Imagegen output | Validation |
|---|---|---|---|---|---|
| `images/15-setting-up-a-dataproc-cluster-05-reports-in-bucket-crisp.png` | `01a1cc28707c611321086bfd4de3be9db38cbf0b6ad74ec32ef8bc953f459cf6` | `c5812061eddc30c2e933e501445c53f79f13a92e201b3d67b9e7e226e811cffb` | `0458cb6048aec80f359e4dfe5fe99f9f8b348e97d13ef1564525f2b59ccd21b5` | Generation artifact was not retained separately; the published PNG contains `gpt-image`/OpenAI C2PA metadata. | Published output unchanged. The retained `535×330` crop keeps the bucket context and both `report-2020/` and `report-2021/` folders; native `1672×941` output hash is recorded. |

The canonical bounded crop is now retained at
`images/15-setting-up-a-dataproc-cluster-05-reports-in-bucket-cropped.png`.
It represents `x=0,y=30,w=535,h=330` in the original `640×360` JPG. The
former `290×660` crop had hash
`244ed5e315d675c9724fa6633c5a6e4ab6617b51e7e1b3ad65a8f6c878f2bab0` and is
retained only as
`images/15-setting-up-a-dataproc-cluster-05-reports-in-bucket-narrow-crop-superseded.png`;
it is not the crop used for provenance or generation.

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
