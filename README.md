import PyPDF2

# Open the PDF file
with open('MultipleFiles/data_science.pdf', 'rb') as file:
    reader = PyPDF2.PdfReader(file)
    text = ''
    for page in reader.pages:
        text += page.extract_text()

# Print the extracted text
print(text)
