# Google Drive Trigger (fileCreated)

This node continuously monitors a chosen Google Drive folder.
How it works:
Whenever a new file (e.g., invoice PDF) is uploaded to the folder, this node triggers the workflow. It ensures automation begins the moment a file is added, eliminating the need for manual starts.

# Download File (Google Drive)
   
This node retrieves the uploaded file so other nodes can process it.
How it works:
Uses the file ID provided by the trigger and downloads the full file (binary data).

# Extract from File (PDF Extractor)
This node extracts raw text from the uploaded PDF.
How it works:
Reads the binary file and converts it into machine-readable text.

# OpenAI Chat Model
This Sub node enhances and interprets the raw text extracted from the PDF.
How it works:
Sends the text to an OpenAI model.The model can clean up data, interpret context, and transform unstructured text into meaningful information.

# Information Extractor
This node identifies and extracts specific details from the AI-processed text.
How it works:
It uses structured prompts or patterns to find key fields (Invoice Number, Customer Name, Email, Phone, Total Amount, Due Date) and outputs them as a clean JSON object.

# Google Sheets (Append or Update Row)
This node saves extracted invoice details into a centralized Google Sheet.
How it works:
Either appends a new row for each invoice or updates existing rows if the invoice already exists.

# Gmail (Send a Message)
This node notifies stakeholders once data has been extracted and saved.
How it works:
Creates a new email message.Inserts extracted invoice details or attaches the processed file.Sends it to a predefined email address.
