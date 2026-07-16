---
layout: default
title: Split Modes
nav_order: 3
---

# Split Modes

**Batch Split PDFs** splits a single PDF into multiple smaller files. The **Pages per file** setting controls how the split works.

---

## Page-by-page split (pages per file = 1)

Set **Pages per file** to `1` to extract every page as its own file.

A 12-page PDF becomes 12 files:

```
document_001.pdf   ← page 1
document_002.pdf   ← page 2
...
document_012.pdf   ← page 12
```

This is useful for:
- Extracting individual slides from a presentation PDF
- Separating scanned documents that were merged together
- Preparing individual pages for upload or sharing

---

## Chunk split (pages per file = N)

Set **Pages per file** to any number greater than 1 to group pages into fixed-size chunks.

A 50-page PDF split into 10-page chunks becomes 5 files:

```
document_001-010.pdf   ← pages 1–10
document_011-020.pdf   ← pages 11–20
document_021-030.pdf   ← pages 21–30
document_031-040.pdf   ← pages 31–40
document_041-050.pdf   ← pages 41–50
```

If the total page count is not evenly divisible, the last chunk contains the remaining pages:

```
document_001-010.pdf   ← pages 1–10
document_011-020.pdf   ← pages 11–20
document_021-023.pdf   ← pages 21–23  (3 pages remaining)
```

---

## Output file naming

Output files are named using the source PDF filename (without extension) plus a zero-padded chunk number or page range:

| Pages per file | Example output names |
|---|---|
| 1 | `report_001.pdf`, `report_002.pdf`, … |
| 10 | `report_001-010.pdf`, `report_011-020.pdf`, … |
| 25 | `report_001-025.pdf`, `report_026-050.pdf`, … |

Zero-padding ensures files sort correctly in filename order in Windows Explorer.

---

## Live preview

Before splitting, the app shows a live count of how many files will be created based on the current **Pages per file** setting and the total page count. This updates as you change the setting so you can experiment before committing. Live preview is available in **Single PDF** mode; in **Folder of PDFs** mode the app instead shows how many PDF files were found in the folder.

---

## Splitting a folder of PDFs

Switch to **Folder of PDFs** mode to split every PDF in a folder in one run, using the same **Pages per file** setting for all of them. Check **Include subfolders** to also process PDFs nested in subfolders of the selected folder.

- All output files, from every source PDF, are written into the single output folder you choose — there are no per-source subfolders.
- If two source PDFs share the same filename (for example, two files both named `report.pdf` found in different subfolders), the app appends a number to one of their output stems (`report_2_001.pdf`) so their outputs don't collide.
- A source PDF that fails to load or split (for example, if it's password-protected) doesn't stop the run — the app skips it, keeps processing the rest of the folder, and lists which files failed once it finishes.
- The finishing summary reports total PDFs processed, total files written, and total pages split across the whole folder.
