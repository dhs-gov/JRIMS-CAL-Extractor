# JRIMS CAL Extractor
[![Python 3.11](https://img.shields.io/badge/python-3.11-blue.svg)](https://www.python.org/downloads/release/python-3114/)

## Code Synopsis
The JRIMS CAL Extractor is a Python script created in Visual Studio Code using the PyPDF2 and Openpyxl libraries to automate extraction of CAL alignments values from pre-existing JRIMS documents. 

## Purpose of the JRIMS CAL Extractor
One of the gaps in DHS's ability to properly assess the impacts of new JRIMS documents is in identifying potential overlap with capability needs identified in previous JRIMS documents. To address this issue, CAL alignment values must be efficiently extracted from these aforementioned documents. Although initial attempts involved manual extraction of the data, the need to expedite the process soon became apparent. With 700+ JRIMS documents left to extract capability data from, this Python-based solution that automated CAL extraction was created by a CTOD intern.

## How to Use


## Next Steps for Development

Notes to Self:
1. Make sure to click the PATH option when reinstalling Python.
2. The saved folder for VSC will be where the PDF documents have to be.
3. Look out for deprecation issues with PyPDF2.
4. Replace the "file" name inside extract_numbers function.
5. Don't stop believing!


Future Areas of Improvement:
- Prevent confusion with Table of Contents values
  - Could skip pages with abnormal amount of qualifying values on it as a solution
