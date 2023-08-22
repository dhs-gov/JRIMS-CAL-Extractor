# JRIMS CAL Extractor
[![Python 3.11](https://img.shields.io/badge/python-3.11-blue.svg)](https://www.python.org/downloads/release/python-3114/)

## Code Synopsis
The JRIMS CAL Extractor is a Python script created in Visual Studio Code using the PyPDF2 and Openpyxl libraries to automate extraction of CAL alignments values from pre-existing JRIMS documents. 

## Purpose of the JRIMS CAL Extractor
One of the gaps in DHS's ability to properly assess the impacts of new JRIMS documents is in identifying potential overlap with capability needs identified in previous JRIMS documents. To address this issue, CAL alignment values must be efficiently extracted from these aforementioned documents. Although initial attempts involved manual extraction of the data, the need to expedite the process soon became apparent. With 700+ JRIMS documents left to extract capability data from, this Python-based solution that automated CAL extraction was created by Justin Oh, a CTOD intern.

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

### 3. After saving the revised Python file, open the Anaconda Command Prompt. Change the directory using the "cd" command to the location of the aforementioned files. <br /><br />
![image](https://github.com/justin-2028/JRIMS-CAL-Extractor/assets/96811261/8b725f8c-4534-461c-8198-76d5d3322e4b)
Above: Anaconda Command Prompt in action.

### 4. Finally, run the command "python [file name].py" to extract the CAL alignment values for each JRIMS document. <br /><br />
![image](https://github.com/justin-2028/JRIMS-CAL-Extractor/assets/96811261/900f82b2-e6ee-4e04-b944-34a09b047550)
Above: CAL alignment values and their corresponding descriptions are outputted per file. Data is censored due to sensitive nature.

## Next Steps for Development
Before widespread usage, the Python script must address an area of concern presented in its output accuracy and also adopt necessary changes to allow outputs to be automatically stored on a separate database for further analysis.  

### 1. Preventing confusion with "Table of Contents" values
The Python script looks for series of four numbers (separated by periods) with similar configurations as CAL alignment values. However, "Table of Contents" values may sometimes qualify under the criteria of the code and be unintentionally outputted. Although the script cross-references an Excel file with official CAL values, there is still a considerable margin of error that must be reduced. A potential idea is to exclude pages with excessive values from the scan to mitigate the "Table of Contents" issue. 
### 2. Options to transfer outputs to a database for real-time analysis 
Storing the outputs into databases such as Mobius is the end goal of this automation project, but is by far the most important future objective. If achieved, the potential visualizations that could be created out of the stored data would be incredibly valuable to DHS.
