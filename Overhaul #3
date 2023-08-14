import re
import PyPDF2
import pandas as pd

def extract_numbers_from_pdf(pdf_file):
    with open(pdf_file, 'rb') as file:
        pdf_reader = PyPDF2.PdfReader(file)

        text = ""

        for page in pdf_reader.pages:
            text += page.extract_text()

        numbers = re.findall(r'\b\d{1,2}\.\d{1,2}\.\d{1,2}(?:\.\d{1,2})?\b', text)
        unique_numbers = set(numbers)

        return unique_numbers

def extract_matching_values_from_excel(excel_file, number_column, description_column, pdf_numbers):
    # Read the Excel file and specify the sheet name
    df = pd.read_excel(excel_file, sheet_name='1-cal', engine='openpyxl')

    # Variable to check if there were any matches
    has_matches = False

    # Iterate through the Excel rows, and compare to the PDF numbers
    for idx, excel_number in enumerate(df[number_column]):
        if excel_number in pdf_numbers:
            print(excel_number, "-", df[description_column][idx])
            has_matches = True

    return has_matches

excel_file = 'FILE.xlsx'  # Replace with your Excel file's name
number_column = 'Number_Column'  # Replace with the number column's name
description_column = 'Description_Column'  # Replace with the description column's name
pdf_files = ['file1.pdf', 'file2.pdf', 'file3.pdf']  # List of your PDF files

for pdf_file in pdf_files:
    print("Processing", pdf_file, ":\n")
    pdf_numbers = extract_numbers_from_pdf(pdf_file)
    has_matches = extract_matching_values_from_excel(excel_file, number_column, description_column, pdf_numbers)

    if not has_matches:
        print("No such values.")

    print("\n\n")  # Two line breaks to separate the outputs
