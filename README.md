## Interview Recording Processor

This application automatically processes interview recordings, transcribes them using OpenAI's Whisper API, analyzes the content with GPT-4, and generates detailed minutes and a summary. The results are formatted as HTML and PDF files, and a summary is sent via email.

## Features
- Automatic detection of today's interview recordings
- Transcription using OpenAI's Whisper API
- Analysis of transcripts to generate minutes and summaries
- Formatted output as HTML and PDF
- Automatic email delivery of results
## Requirements
- Python 3.8+
- OpenAI API key
- Gmail account for sending emails
- wkhtmltopdf (for PDF generation)
## Installation
- Clone this repository
- Install dependencies:
pip install -r requirements.txt
- Install wkhtmltopdf:
    - Windows: Download from wkhtmltopdf.org
    - macOS: brew install wkhtmltopdf
    - Linux: sudo apt-get install wkhtmltopdf
- Copy .env.sample to .env and fill in your API key and email credentials
