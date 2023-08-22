# JRIMS CAL Extractor
[![Python 3.11](https://img.shields.io/badge/python-3.11-blue.svg)](https://www.python.org/downloads/release/python-3114/)

## Code Synopsis
The JRIMS CAL Extractor is a Python script created in Visual Studio Code using the PyPDF2 and Openpyxl libraries to automate extraction of CAL alignments values from pre-existing JRIMS documents. 

## Purpose of the JRIMS CAL Extractor
One of the gaps in DHS's ability to properly assess the impacts of new JRIMS documents is in identifying potential overlap with capability needs identified in previous JRIMS documents. To address this issue, CAL alignment values must be efficiently extracted from these aforementioned documents. Although initial attempts involved manual extraction of the data, the need to expedite the process soon became apparent. With 700+ JRIMS documents left to extract capability data from, this Python-based solution that automated CAL extraction was created by a CTOD intern.

## How to Use
Throughout these instructions, Anaconda Navigator will be used due to its compatbility with DHS laptops. The majority of commonly used Python libraries are pre-installed with Anaconda, although PyPDF2 is a noteworthy exception. All of the following directions are possible through the conventional method of downloading Python libraries (PyPDF2, openpyxl) through PIP and running the script through Visual Studio Code's terminal. <br /><br />
![image](https://github.com/justin-2028/JRIMS-CAL-Extractor/assets/96811261/d0ba5988-0d09-407a-98aa-9423d1421e80)
Above: Several packages available through the Anaconda Navigator.

### 1. Download the latest version of the JRIMS CAL Extractor and store them in the same file directory as the JRIMS PDF documents that require scanning. If available, store an Excel file of official CAL alignment values in this directory as well. <br /><br />
![image](https://github.com/justin-2028/JRIMS-CAL-Extractor/assets/96811261/7613edae-8036-4aff-9208-c903f4eb71ed)
Above: The Python script, CAL Alignments Excel file and three JRIMS documents are stored in the same directory.

### 2. Open the Python file in Visual Studio Code and provide the following information:
##### •	Name of the Excel file <br />
##### •	Column containing CAL alignment values in the Excel file <br />
##### •	Column containing CAL alignment descriptions in the Excel file <br />
##### •	Name(s) of the JRIMS documents that will be scanned <br /><br />
![image](https://github.com/justin-2028/JRIMS-CAL-Extractor/assets/96811261/04bbd6e7-5899-4ee0-9aaf-202f7d514409)
Above: Revised code containing the details needed for the scanning process of three JRIMS documents.

### 3. f
### 4. f
### 5. f
### 6. f
### 7. f
### 8. f

## Next Steps for Development
Before widespread usage, the Python script must address an area of concern presented in its output accuracy and also adopt necessary changes to allow outputs to be automatically stored on a separate database for further analysis.  

Notes to Self:
1. Make sure to click the PATH option when reinstalling Python.
2. The saved folder for VSC will be where the PDF documents have to be.
3. Look out for deprecation issues with PyPDF2.
4. Replace the "file" name inside extract_numbers function.
5. Don't stop believing!


Future Areas of Improvement:
- Prevent confusion with Table of Contents values
  - Could skip pages with abnormal amount of qualifying values on it as a solution
