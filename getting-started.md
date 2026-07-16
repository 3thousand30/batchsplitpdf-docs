---
layout: default
title: Getting Started
nav_order: 2
---

# Getting Started

This guide walks you through splitting your first PDF using **Batch Split PDFs**.

---

## 1. Install the app

Download and install **Batch Split PDFs** from the Microsoft Store. Once installed, launch it from the Start menu.

---

## 2. Select a PDF file, or a folder of PDFs

Choose **Single PDF** or **Folder of PDFs** at the top of the window.

- **Single PDF** — click **Browse** next to **PDF file** and select the PDF you want to split. The app reads the file and shows the total page count.
- **Folder of PDFs** — click **Browse** next to **Folder** and select a folder. Every PDF directly inside is split using the same **Pages per file** setting. Check **Include subfolders** to also process PDFs nested in subfolders. The app shows how many PDFs were found before you split.

---

## 3. Set pages per file

Use the **Pages per file** control to choose how many pages go into each output file.

- Set to **1** to get one PDF per page
- Set to **10** to get one PDF per 10 pages (a 100-page PDF becomes 10 files)

In **Single PDF** mode, the app shows a live preview of how many files will be created based on your setting.

---

## 4. Choose an output folder

The output folder is where the split files will be saved. It defaults to `Documents\BatchSplitPDFs`.

Click **Browse** to choose a different location.

---

## 5. Set options

- **Skip files that already exist** — if checked, any chunk that already exists in the output folder is skipped. Useful for resuming a split without re-processing completed chunks.

---

## 6. Split

Click **Split PDF**. A progress bar shows each chunk being written. When done, click **Open folder** to see the output files.

In **Folder of PDFs** mode, all output files from every source PDF are saved into the same output folder. If two source PDFs share the same name (common when including subfolders), the app automatically disambiguates their output names so files don't overwrite each other. If some files in the folder fail to split, the app still processes the rest and reports which ones failed when it finishes.

---

## Output file naming

Output files are named after the source PDF with a zero-padded chunk number appended:

```
report_001.pdf
report_002.pdf
report_003.pdf
```

For single-page splits, each file is named `document_001.pdf`, `document_002.pdf`, and so on. For chunk splits, the name reflects the page range: `document_001-010.pdf`, `document_011-020.pdf`.

See [Split Modes](split-modes) for more detail.
