# Automated Log Analysis System

A desktop application for scanning and analyzing log files to detect errors and provide solutions using a mapping table. Built for academic and non-commercial use. Built with the help of APRO company's provided data.

---

##  Features

- Manual or automatic keyword-based log analysis
- Supports multiple `.json` log files
- Help function to display cause and corrective actions for known error codes
- GUI built with PyQt5
- Offline, fast, and simple to use

---

##  How It Works

###  Log File Analysis
- **Manual Mode:** Enter one or more keywords (comma-separated) to search within selected `.json` log files.
- **Automatic Mode:** Automatically scans for a default keyword (e.g., `EALM`).
- Results are displayed in a table showing:
  - File name
  - Line number
  - Matching line content
  - Click to view full log file with highlight

###  Help Function
- Enter an error code in the Help section.
- The system looks it up in the `mapping_table.csv`.
- If found, it displays:
  - **Cause** of the error
  - **Corrective actions**
- If not found, shows: `"No matched error code"`

---

##  Tech Stack

| Component       | Technology       |
|----------------|------------------|
| Language        | Python 3         |
| GUI             | PyQt5            |
| File Handling   | `os`, `pathlib`  |
| Pattern Matching| `re` (regex)     |
| Log File Format | `.json`          |
| Mapping Table   | `.csv` (Excel-compatible) |

---


## Example UI Screens

 | Mode	          |               Description              |
 |----------------|----------------------------------------|
 |Search File	    | Choose and scan one or more .log files |
 |Manual Search  	| Input custom keywords                  | 
 |Auto Search	    | Use default Word (e.g., EALM)          |
 |Help	Input     | error code and retrieve cause/solution |

 ## Requirements

- Python 3.10 or higher
- PyQt5
- pandas

 ## Installation Guide

Follow these steps to install and run the Automated Log Analysis System on your machine.

###  Prerequisites

Make sure you have the following installed:

- [Python 3.10+](https://www.python.org/downloads/)
- `pip` package installer (comes with Python)

---

###  Step 1: Clone the Repository

If you haven’t already, clone this project from GitHub:

git clone https://github.com/Alexus-27/automated-log-analysis.git
cd automated-log-analysis

### Step 2: Create a virtual environment (Recommended)
python -m venv venv
# Activate the virtual environment:
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

### Step 3: Install required libraries
pip install pyqt5 pandas


### Step 4: Prepare Project Files
Ensure the following files/folders are correctly placed:

main.py — in the root directory

mapping_table.csv — in the root directory

logs/ folder — contains your .json log files in the root directory

### Step 5: Run the application
Once ecerything is setup, run the application with 
python main.py
This will launch the PyQt5 GUI for log analysis.

### Troubleshooting
No GUI appears? Make sure your Python environment is activated and PyQt5 is installed correctly.

File not found errors? Check that mapping_table.csv and log files are in the correct paths.



## Development Timeline

| Month	|              Milestone                 |
|-------|----------------------------------------|
|March	| Planning & Requirements Gathering      |
|April	| High-Level and Low-Level Design        |
|May	  | Development & Testing                  |
|June	  | Final Integration, Documentation, Demo |

## Team

|Name	                   |                  Role               |  Student ID |
|------------------------|-------------------------------------|-------------|
|Aleksandr Atakov		     |Team Leader, Developer               | 202412042   |
|Aleksandr Avdeev		     |Graphhical Interface Designer, Tester| 202412027   |
|Muhammad Mubashir		   |Low Level Designer, Support          | 202412120   |
|Rachel Grajeda Angulo	 |Team Leader, Tester                  | 202412182   |

## Testing
 Manual log testing with APRO’s sample logs

 Unit testing on keyword detection and Help module

 Integration testing for UI navigation and file handling


### License
This project is for academic and non-commercial use. For deployment in industrial settings or licensing, contact the developers or APRO directly.

## Acknowledgments
Professor Lim We Cheol – Project Supervisor

APRO – Industry partner, advisor, and data provider

