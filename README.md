# PDF Section Summarizer with LLM
### Intelligent Document Analysis & Summarization Tool

## Overview
This Python-based tool automatically processes PDF documents, identifies sections based on text formatting, and generates intelligent summaries using a Local Large Language Model (LLM). The summaries are then compiled into a well-structured Word document.

## Features
- PDF text extraction with formatting awareness
- Automatic section detection based on font size
- Intelligent text summarization using Local LLM
- Word document generation with formatted summaries
- Special character handling for API compatibility
- Progress tracking during processing

## Requirements
```python
PyMuPDF>=1.18.0
python-docx>=0.8.11
subprocess
json
```


## Usage
```python
from pdf_summarizer import read_pdf_and_summarize

# Basic usage
read_pdf_and_summarize("input.pdf", "output.docx")

# Start from specific page
read_pdf_and_summarize("input.pdf", "output.docx", start_page=5)
```

## API Configuration
The tool requires a local LLM API running on port 1234. But you could also use an external API.


## Text Processing Rules
- Sections are identified by font size > 13
- Minimum 35 words required for summarization
- Text chunks limited to 1900 words per API call

## Error Handling
- JSON decode error management
- API communication error handling
- Empty response handling
- Unicode character sanitization

## Contributing
1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details.


#DocumentProcessing #MachineLearning #PDF #Python #LLM

Note: Make sure your local LLM API is properly configured before running the tool, i use llmstudio