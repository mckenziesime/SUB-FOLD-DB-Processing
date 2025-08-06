# SUB-FOLD-DB-Processing

**SUB-FOLD-DB-Processing** is a Python-based processing tool for converting database (`.db`) files exported from the Time Sync Plus (TSPO) application into the CSV format required for Google Earth Engine (GEE) upload.  
It also supports optional formatting steps to prepare descriptive statistics and restructured probability tables for interpreter observation analysis.

---

## Features

- **Batch Database to CSV Conversion**  
  Converts multiple `.db` files from TSPO into CSV format, organized by table type.

- **Table Consolidation**  
  Merges all database outputs into three standardized CSVs:  
  *Display Table*, *Event Table*, and *Polygon Table*.

- **Interpreter Observation Reformatting**  
  Expands and separates loss, stable, and growth probability values for each epoch.

- **Data Cleaning & Deduplication**  
  Removes repeated observations caused by entry errors.

- **Metadata Integration**  
  Merges event observations with point metadata from the Polygon Table, including coordinates and stratum IDs.

- **Probability Summaries**  
  Generates average and most-recent probability columns for each user, plus loss/no-loss (True/False) fields.

- **Google Earth Engine–Ready Outputs**  
  Produces GEE-compatible CSVs for both per-user and combined-observation formats.

---

## Technologies Used

- **Language**: Python (≥3.9 recommended)
- **Libraries**:  
  - `sqlite3` – Database connection & querying  
  - `pandas` – Data manipulation & export  
  - `numpy` – Numeric operations  
  - `json` & `re` – JSON parsing & regular expressions  
  - `os` – File path handling

---

## Project Structure
SUB-FOLD-DB-Processing/

├── reformat_interpreter_obs.py # Main processing script

├── README.md # Project documentation

├── requirements.txt # Python package dependencies

└── output/ # Processed CSV outputs

---

## Application Setup

### 1. Install Python Environment
It is recommended to create a dedicated Python environment.

```bash
conda create -n subfold_env python=3.10
conda activate subfold_env
pip install -r requirements.txt
```
---

## Notes:

- Feel free to submit issues or pull requests for improvements to documentation.
