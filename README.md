# Business Value Consultant

An AI-powered web application that helps analyze business documents and articulate value propositions, outcomes, and KPIs using Google's Gemini API.

## Features

- **Document Analysis**: Upload Value Maps (images or text) and Solution Documents to provide context
- **Braze Value Cards Reference**: Store constant reference materials with standard metrics and benchmarks
- **Quick Actions**: One-click analysis for common business scenarios:
  - 🔍 **Current State & Pain Points** - Identifies challenges with business impact
  - 🚀 **Future State & Outcomes** - Maps solutions to Value Map goals
  - 📈 **Suggested KPIs** - Recommends metrics with measurement methods
  - 🔀 **Generate Diagram CSV** - Creates Lucidchart-compatible architecture diagrams
- **Persistent Storage**: API key and reference materials saved to browser localStorage

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- A [Google Gemini API key](https://aistudio.google.com/app/apikey)

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/seshankanagasabai/BVF_Assistant.git
   cd BVF_Assistant
   ```

2. **Start a local server**
   ```bash
   # Using Python 3
   python3 -m http.server 8080
   
   # Or using Python 2
   python -m SimpleHTTPServer 8080
   
   # Or using Node.js (if installed)
   npx serve
   ```

3. **Open in browser**
   ```
   http://localhost:8080/AI%20OKR/gemini-chat.html
   ```

4. **Configure the app**
   - Enter your Gemini API key and click "Save Key"
   - (Optional) Add Braze Value Cards reference content
   - Upload your Value Map and Solution Document

## Usage Guide

### Step 1: API Key Setup
1. Get a free API key from [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Paste it in the "API Key" field
3. Click "Save Key" - it will be stored in your browser

### Step 2: Add Reference Materials (Optional)
1. Click "Braze Value Cards Reference" to expand
2. Paste your standard value metrics and benchmarks
3. Click "Save Reference" - this persists across sessions

### Step 3: Upload Documents

**Value Map** (Customer's business goals):
- Supports: PNG, JPG, JPEG, WebP images OR text/markdown files
- Tip: Export Google Slides as PNG images

**Solution Document** (Proposed solution):
- Supports: HTML, text, markdown OR PNG/JPG images
- Tip: Export Google Docs as HTML (File → Download → Web Page)

### Step 4: Analyze

Use the quick action buttons or type your own questions:

| Button | Output |
|--------|--------|
| Current State & Pain Points | 3-5 bullet points of key challenges |
| Future State & Outcomes | 3-5 bullets linking Value Map goals to solutions |
| Suggested KPIs | 3-5 KPIs with targets and measurement methods |
| Generate Diagram CSV | Lucidchart-compatible CSV for architecture diagrams |

### Importing Diagrams to Lucidchart

1. Click "Generate Diagram CSV"
2. Download the CSV file
3. In Lucidchart: File → Import Data → CSV
4. Map the columns and generate your diagram

## File Structure

```
BVF_Assistant/
├── README.md
└── AI OKR/
    └── gemini-chat.html    # Main application (single HTML file)
```

## Technical Details

- **Frontend**: Vanilla HTML, CSS, JavaScript (no frameworks)
- **AI Model**: Google Gemini 2.0 Flash
- **Storage**: Browser localStorage for API key and reference materials
- **Multimodal**: Supports image analysis for Value Maps and Solution Docs

## Privacy & Security

- Your API key is stored only in your browser's localStorage
- Documents are sent directly to Google's Gemini API
- No data is stored on any server
- All processing happens client-side

## Troubleshooting

| Issue | Solution |
|-------|----------|
| "Invalid API key" | Check your Gemini API key at [Google AI Studio](https://aistudio.google.com/app/apikey) |
| "Network error" | Check your internet connection |
| Buttons disabled | Make sure API key is saved |
| No diagram generated | Ensure Solution Document is uploaded |

## License

This project is for internal use.

---

Built with ❤️ using Google Gemini AI
