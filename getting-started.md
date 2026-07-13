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

## 2. Select a PDF file

Click **Browse** next to **PDF file** and select the PDF you want to split.

The app reads the file and shows the total page count. This helps you decide how to split it.

---

## 3. Set pages per file

Use the **Pages per file** control to choose how many pages go into each output file.

- Set to **1** to get one PDF per page
- Set to **10** to get one PDF per 10 pages (a 100-page PDF becomes 10 files)

The app shows a live preview of how many files will be created based on your setting.

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
