# IT23712690 - Sheshanthan P

# IT23712690 - Automated Translation Testing

## Project Overview

This project automates the testing of a Sinhala chat translator web application ([pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator)). It uses Python and Playwright to automatically input Singlish (Sinhala written in English) test cases, capture the translated output, compare it against expected results, and record the status in an Excel file.

---

## Project Structure

---

## Test Case File Structure

The Excel file (`IT23712690.xlsx`) contains the following columns:

| Column | Description |
|---|---|
| Test Case ID | Unique identifier (e.g., Neg_0001) |
| Input length type | S = Short, M = Medium, L = Long |
| Input | Singlish input text |
| Expected output | Expected Sinhala translation |
| Actual output | Actual translation captured from the website |
| Status | PASS or FAIL based on comparison |

---

## Requirements

- Python 3.x
- Playwright
- openpyxl

Install dependencies:

\```bash
pip install playwright openpyxl
playwright install
\```

---

## How to Run

1. Open **VS Code as Administrator** (right-click → Run as administrator)
2. Open the terminal and navigate to the project folder:

\```powershell
cd D:\IT23712690
\```

3. Run the script:

\```powershell
python IT23712690.py --excel "D:\IT23712690\IT23712690.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
\```

---

## Command Line Arguments

| Argument | Description | Default |
|---|---|---|
| `--excel` | Path to the Excel test cases file | Required |
| `--url` | URL of the translator to test | Required |
| `--wait-ms` | Wait time in ms after each input | 5000 |
| `--type-delay-ms` | Delay between keystrokes in ms | 80 |
| `--slow-mo-ms` | Slow motion delay for browser actions | 200 |
| `--save-every` | Save results every N rows | 1 |
| `--keep-open` | Keep browser open after test completes | False |
| `--headless` | Run browser in headless mode | False |

---

## Test Case Categories

The test cases cover a wide range of Singlish inputs including:

- Everyday casual conversations
- Questions and responses
- Mixed language (Singlish + English words)
- Special characters and punctuation
- Emojis
- Numbers, currency, dates, and times
- URLs and technical terms
- Short (S), Medium (M), and Long (L) length inputs

---

## Notes

- Make sure the Excel file is **closed** before running the script to avoid permission errors.
- Run VS Code as **Administrator** to avoid file write permission issues.
- Long inputs (type L) may occasionally cause UI delays on the translator website.