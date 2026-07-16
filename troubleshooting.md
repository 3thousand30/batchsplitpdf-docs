---
layout: default
title: Troubleshooting
nav_order: 4
---

# Troubleshooting

Common issues and how to fix them.

---

## The PDF page count shows as 0 or does not appear

- Make sure the selected file is a valid PDF — try opening it in a PDF viewer first
- Password-protected PDFs cannot be read; remove the password protection first
- Very old or non-standard PDF formats may not be supported

---

## Split fails for a specific chunk

- The source PDF may be corrupted — try opening it in a PDF viewer and saving a fresh copy
- If the file is very large, ensure you have enough disk space in the output folder
- Try splitting a smaller range first to isolate which pages cause the issue

---

## Splitting a folder: some files failed but others worked

In **Folder of PDFs** mode, a file that fails to load or split (for example, a password-protected PDF) doesn't stop the batch — the app skips it and keeps going. Check the finishing summary for the list of failed files, fix or remove them, and rerun with **Skip files that already exist** checked to avoid re-processing what already succeeded.

---

## Output files are in the wrong order

Output files are named with zero-padded numbers (`001`, `002`, …) so they sort correctly alphabetically in Windows Explorer. If files appear out of order, check that your file explorer is sorting by **Name** (not by date or size).

---

## Output file already exists

If **Skip files that already exist** is checked, the app skips chunks that are already present in the output folder. Uncheck this option to overwrite existing files, or delete the existing output files first.

---

## Output folder cannot be created

- Check that you have write permission to the output location
- Avoid network drives or synced folders (OneDrive, Dropbox) as the output location — use a local path such as `Documents\BatchSplitPDFs` instead

---

## App won't start or crashes on launch

- Check that Windows is up to date; the app requires Windows 10 or later
- Reinstall the app from the Microsoft Store if the issue persists

---

## Still stuck?

Email [hello@3thousand30.com](mailto:hello@3thousand30.com) or [open an issue](https://github.com/3thousand30/batchsplitpdf-docs/issues) with the error message and a description of the PDF you were splitting.
