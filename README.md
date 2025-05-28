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
## Configuration
Create a .env file with the following information:

```bash
    OPENAI_API_KEY=your_openai_api_key_here
    EMAIL_SENDER=your_gmail_address@gmail.com
    EMAIL_PASSWORD=your_gmail_app_password
    EMAIL_RECIPIENT=recipient@example.com
```

For Gmail, you need to use an App Password instead of your regular password. See .env.sample for instructions.

## Usage

1. Place your recording files in a folder named "Recordings" in the project directory
2. Make sure recording filenames start with today's date in YYYY-MM-DD format
3. Run the script:

    ```bash 
    python code/meeting_recorder.py
    ```

4. Check the "Output" folder for the generated files

## Output

The script generates the following files for each processed interview:

- HTML and PDF versions of detailed minutes
- HTML and PDF versions of a concise summary
- Email with the summary and minutes attached

