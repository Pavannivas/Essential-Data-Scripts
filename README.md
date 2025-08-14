# Essential Data Scripts for Busy Professionals

Time-saving Python scripts for automating repetitive data science tasks.
Five Python scripts useful for data science tasks. 
Stop wrestling with repetitive tasks and focus on actual analysis.


### Data Quality Checker
- The pain point: Opening a new dataset often feels overwhelming. Are there missing values? Duplicates? Weird data types? You end up writing the same exploratory code over and over, or worse, discovering data issues after hours of analysis.
- What the script does: A simple Python script to process a given dataframe and generate a concise data quality report with info on missing values, duplicates, outliers, and more. Then saves everything to a readable text file you can refer to as needed.
- How it works: The script systematically checks for common data quality issues — duplicates, missing values, incorrect data types — using pandas built-in methods, calculates percentages and statistics, then formats everything into a clean report. It uses the interquartile range (IQR) method for outlier detection, which works reliably across different data distributions.

### Smart File Merger
- The pain point: Your data is in CSV files, Excel sheets, and JSON exports scattered across folders. Combining them manually means opening each file, checking column alignment, copy-pasting, and praying nothing breaks. Yeah, and one mismatched column is enough to ruin everything.
- What the script does: Automatically finds and combines all data files in a folder, regardless of format (CSV, Excel, JSON). Handles column mismatches gracefully and tracks which data came from which source file.
- How it works: The script walks through a directory, identifies supported file types, uses the appropriate pandas reader for each format, and concatenates everything using pandas' robust merging logic. It adds a source column so you can always trace data back to its origin.

### Dataset Profiler
- The pain point: Understanding a new dataset requires writing dozens of lines of exploratory code: describe(), value_counts(), correlation matrices, missing value analysis. By the time you finish exploring, you've probably forgotten what you were trying to analyze.
- What the script does: Generates a complete dataset profile in seconds, including summary statistics, correlation heatmaps, categorical breakdowns, and memory optimization suggestions. Creates helpful visualizations for documentation and reporting.
- How it works: The script separates numeric and categorical columns, applies appropriate analysis methods to each type, generates visualizations using seaborn and matplotlib, and also provides actionable optimization recommendations based on data patterns.

### Data Version Manager
- The pain point: You make changes to your dataset, realize something went wrong, and have no way back. Or you need to show a client what the data looked like last week, but you've been overwriting the same file. Version control for data is often challenging. There are tools to simplify data version control. But simple Python scripts are, well, simpler and effective, too.
- What the script does: Automatically saves timestamped versions of your DataFrames with descriptions, tracks file hashes to detect changes, and lets you roll back to any previous version instantly. Includes cleanup tools to manage storage space.
- How it works: The script creates a structured backup system with metadata logging. It uses MD5 hashing to detect actual changes (avoiding duplicate saves), maintains a CSV log of all versions with timestamps and descriptions, and provides simple methods to list and restore any previous version.

### Multi-Format Data Exporter
- The pain point: Different people want data in different formats. The analysts probably want clean spreadsheets with formatted headers. The dev team needs JSON with metadata. The database admin wants SQLite. You end up manually creating each format with different settings and formatting rules.
- What the script does: Exports your processed data to multiple professional formats simultaneously. Creates formatted Excel files with multiple sheets, structured JSON with metadata, clean CSV files, and SQLite databases with proper schemas.
- How it works: The script uses format-specific optimization techniques: Excel files get styled headers and auto-sized columns, JSON exports include metadata and proper data type information, CSV files are cleaned to avoid delimiter conflicts, and SQLite databases include metadata tables for complete documentation.

## Requirements

- Python 3.7+
- pandas
- numpy
- matplotlib
- seaborn
- openpyxl

## Installation

```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

Or use the provided requirements file:
```bash
pip install -r requirements.txt
```