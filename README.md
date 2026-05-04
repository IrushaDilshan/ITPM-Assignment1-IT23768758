# Transliteration Accuracy Testing (Singlish to Sinhala)

## Project Overview & Objective
This project is an automated testing suite developed for ITPM Assignment 1. The primary objective is to test the 'Chat Sinhala' transliteration function on [Pixels Suite Chat Translator](https://www.pixelssuite.com/chat-translator) by automating English/Singlish to Sinhala character conversions and verifying their accuracy against an expected outcome. Through this automation process, the suite successfully identifies 51 failed test cases (out of 52 total test cases) to evaluate and highlight inaccuracies in the transliteration engine. 

## Prerequisites
Before executing the automation script, assure that your system meets the following requirements:
* **Python**: Python 3.7 or higher installed on your machine.
* **Web Browser**: Google Chrome (or a Chromium-based browser) installed.
* **Operating System**: Windows / macOS / Linux.

## Installation Guide
You will need to install a few dependencies to run the test script. Open your terminal or command prompt, navigate to the project directory, and execute the following commands:

1. **Install Playwright** (for browser automation):
   ```bash
   pip install playwright
   ```
2. **Install OpenPyXL** (for reading and writing Excel files):
   ```bash
   pip install openpyxl
   ```
3. **Install Playwright Browsers**:
   ```bash
   playwright install chromium
   ```

## How to Run the Automation Script
To run the automation script, execute the following command in your terminal from the root folder of the project:

```bash
python test_automation.py --excel "IT23768758_Assignment1.xlsx" --url "https://www.pixelssuite.com/chat-translator" --headless
```

### Available Command-Line Flags:
* `--excel`: Path to the Excel file containing the test cases (`IT23768758_Assignment1.xlsx`).
* `--url`: The target URL to test (`https://www.pixelssuite.com/chat-translator`).
* `--headless`: Start Playwright in headless mode (running in the background without UI). Omit for visual debugging.
* `--sheet`: The name of the sheet inside the Excel file (default is " Test cases").
* `--output`: Output Excel file path. If not specified, it overhangs/modifies the provided input file.
* `--retries`: Retries for element location (default: 8).
* `--timeout-ms`: Maximum timeout to wait in milliseconds (default: 60000).

## Folder Structure Description
* `IT23768758_GitLink.txt`: A text file containing the URL link to the GitHub repository where this project is hosted.
* `test_automation.py`: The main Python script utilizing Playwright to extract test data from Excel, perform transliterations on the target site, and record outcomes back into the Excel file.
* `IT23768758_Assignment1.xlsx`: The Excel workbook containing the test cases (Input, Expected Output, Actual Output, Status).

## Author Details
* **Name**: Vidanapathirana I.D
* **Reg No**: IT23768758
* **University**: SLIIT 
* **Program**: 3rd Year IT Student