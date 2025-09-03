# ATS Resume Scanner

An intelligent Application Tracking System (ATS) powered by Google's Gemini AI that analyzes resumes against job descriptions to help job seekers optimize their applications.

## Features

- **Resume Analysis**: Get professional evaluation of your resume against job requirements
- **Keyword Extraction**: Identify missing technical, analytical, and soft skills
- **Match Percentage**: Calculate compatibility score between resume and job description
- **PDF Processing**: Upload and analyze PDF resumes
- **Real-time Results**: Instant AI-powered feedback

## Prerequisites

- Python 3.7 or higher
- Google Cloud Console account (for Gemini API key)
- Git

## Installation

### Step 1: Download Code
```bash
git clone https://github.com/mohibali03/gemini-resume-scanner.git
```

### Step 2: Navigate to Project Directory
```bash
cd gemini-resume-scanner
```

### Step 3: Create Virtual Environment
```bash
python -m venv venv
```

**Activate Virtual Environment:**

Windows:
```bash
venv\Scripts\activate
```

Linux/Mac:
```bash
source venv/bin/activate
```

### Step 4: Install Dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
pip install google-generativeai
```

## Configuration

### Step 5: AI Gemini Setup

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project or select an existing one
3. Enable the Gemini API
4. Create an API key

### Step 6: Configure Streamlit Secrets

Create the secrets directory and file:

```bash
mkdir -p .streamlit
```

Create the secrets configuration:
```bash
echo 'GOOGLE_API_KEY = "your-api-key-here"' > .streamlit/secrets.toml
```

**Important**: Replace `"your-api-key-here"` with your actual Google API key.

## Running the Application

Start the Streamlit application:

```bash
streamlit run app.py --server.port 8501 --server.enableCORS false
```

The application will be available at: `http://localhost:8501`

## Usage

1. **Enter Job Description**: Paste the job description in the text area
2. **Upload Resume**: Upload your PDF resume
3. **Choose Analysis Type**:
   - **Tell Me About the Resume**: Get professional evaluation
   - **Get Keywords**: Extract required skills and keywords
   - **Percentage Match**: Get compatibility score and missing keywords

## Project Structure

```
Gemini-resume-scanner/
│   ├── app.py              # Main Streamlit application
│   ├── requirements.txt    # Python dependencies
│   ├── packages.txt        # System packages
│   └── index.html         # Additional HTML file
├── .streamlit/
│   └── secrets.toml       # API configuration (create this)
└── README.md              # This file
```

## Dependencies

- **streamlit**: Web application framework
- **google-generativeai**: Google Gemini AI integration
- **pdf2image**: PDF to image conversion
- **PyPDF2**: PDF processing
- **Pillow**: Image processing
- **numpy**: Numerical computing
- **pandas**: Data manipulation

## Troubleshooting

### Common Issues

1. **API Key Error**: Ensure your Google API key is correctly set in `.streamlit/secrets.toml`
2. **PDF Upload Issues**: Make sure the uploaded file is a valid PDF
3. **Port Already in Use**: Change the port number in the run command (e.g., `--server.port 8502`)

### System Requirements

- Ensure `poppler-utils` is installed for PDF processing
- On Windows, you might need to install poppler separately

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

For issues and questions, please create an issue in the GitHub repository.

---

**Note**: Keep your API keys secure and never commit them to version control.
