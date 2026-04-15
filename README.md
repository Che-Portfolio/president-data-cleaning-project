# President Data Cleaning Excel Project

Excel-based data cleaning and analysis project using a U.S. presidents dataset.

## Project goals

- Practice cleaning messy real-world style data in Excel.
- Engineer useful features (flags and groupings) for analysis.
- Build simple summaries and KPIs using PivotTables.

## Dataset

- Source: US Presidents Excel tutorial data (Washington through Trump).
- Rows: 45 records, one row per presidency in the source file.
- Scope/limitations:
  - Ends at Donald Trump (Joe Biden not included in source).
  - Original file double-counted Woodrow Wilson and had party typos.
  - Salaries are simplified and increase in a pattern, not historical numbers.

## Cleaning steps

Working in the `Working` sheet:

- Standardized text fields:
  - Cleaned `president`, `party`, and `vice` names using TRIM/PROPER.
  - Fixed misspellings (e.g. `Demorcatic` → `Democratic`).
  - Normalized historical party labels (e.g. `Democratic-  Republican` → `Democratic-Republican`).
- Converted salary:
  - Turned text salary values (e.g. `$405,000.00`) into numeric `salary_num_clean`.
- Engineered fields:
  - `HighSalary` flag based on salary threshold.
  - `party_final` (clean party labels).
  - `party_type` (Major = Democratic/Republican, Other = all other parties).
- Structural fixes:
  - Removed duplicate Woodrow Wilson row from the working table.
  - Sorted by `S.No.` so records follow the source presidency order.

## Analysis and outputs

Using PivotTables and formulas:

- Total salary by party (`total salary by party_clean` / `Summary`).
- Average president salary by party and by `party_type`.
- High vs Normal salary counts by `party_type`.
- % of HighSalary presidents by `party_type` (calculated outside the pivot).

These outputs are intended as a small KPI-style view rather than a full dashboard.

## Files

- `President Data Cleaning Excel Project.xlsx`  
  Main Excel file containing:
  - `US_Presidents Excel Tutorial Da` (raw source data).
  - `Working` (cleaned / engineered dataset).
  - Pivot sheets for totals, averages, and High vs Normal.
  - `Summary` for simple party-level totals.

## Notes

This project is focused on practicing Excel data cleaning, feature engineering, and basic analysis on a small dataset, not on historical accuracy of salaries or a complete presidential list.
