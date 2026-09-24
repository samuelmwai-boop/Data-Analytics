# Lesson Summary: Spreadsheet Functions & Descriptive Statistics

**Date:** September 24, 2026

## Topics Covered

### 1. Spreadsheet File Formats
- Reviewed how spreadsheets store data in rows/columns *plus* formatting, formulas, and other properties (unlike plain text formats).
- Covered when **separator/delimiter** settings matter during import — specifically for plain-text formats like `.txt`, `.csv`, and `.tsv`, since these rely on a character (comma, tab, etc.) to define columns.
- Native formats like `.xls` and `.xlsx` don't need separator settings, since their structure is already built in.

### 2. Descriptive Statistics — Concepts
- **Definition:** Tools that summarize and describe the main features of a dataset (central tendency, variability, shape) without drawing broader conclusions.
- **Why they matter:** Quick data snapshots, early error/outlier detection, guidance on which deeper analysis methods are appropriate, and context for interpreting results.
- **Risk of ignoring variability:** Averages alone can hide big disparities (e.g., household income), leading to poor decisions, missed subgroups, false confidence, and outlier distortion.

### 3. Core Spreadsheet Functions

| Function | Purpose | Example |
|----------|---------|---------|
| `SUM` | Adds values in a range | `=SUM(D14:D19)` |
| `COUNT` | Counts numeric values only | `=COUNT(D14:D19)` |
| `COUNTA` | Counts any non-empty cell (numbers, text, etc.) | `=COUNTA(D14:D19)` |
| `MIN` | Finds the smallest value | `=MIN(D14:D19)` |
| `MAX` | Finds the largest value | `=MAX(D14:D19)` |
| `AVERAGE` | Calculates the mean | `=AVERAGE(D14:D19)` |

### 4. How Data Quality Issues Affect These Functions
- **Empty cells:** Ignored by SUM, COUNT, MIN, MAX — no error, but can silently understate results if unexpected.
- **Text values:** Also ignored (not counted/summed) — a common trap when numeric columns contain stray text like "N/A."
- **Errors (#N/A, #VALUE!, etc.):** These **propagate** — the whole formula breaks and returns an error until fixed (e.g., via `IFERROR()`).
- **COUNT vs. COUNTA:** Use `COUNT` for numeric-only tallies; use `COUNTA` to count all non-blank entries regardless of type — comparing the two is a fast way to spot data quality issues.

## Key Takeaways
- Always verify separator settings when importing plain-text data files.
- Spreadsheet formats preserve much more than raw values — formatting and formulas matter.
- Descriptive statistics are a first step, not a final answer — variability is just as important as central tendency.
- SUM/COUNT/MIN/MAX are simple but powerful — just be aware of how blanks, text, and errors quietly (or not-so-quietly) affect results.
