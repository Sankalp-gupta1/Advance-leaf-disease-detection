# Advanced Leaf Disease Detection

A plant-image analysis project with two modes:

1. a **live no-key browser demo** for portfolio use,
2. the original **FastAPI + Groq vision** implementation for environments where a valid API key is configured.

## Live demo

**https://leaf-disease-detection-demo.vercel.app/**

The public demo is designed to be honest and easy to run.

It does **not** pretend to run a private Groq vision model without credentials.

Instead, it performs client-side visual analysis of the uploaded leaf image and reports:

- green-pixel share,
- yellowing share,
- brown/dry-looking share,
- a simple visual-stress index,
- image preview and analysis summary.

The uploaded image is processed in the browser for the hosted demo.

## Important limitation

The hosted demo is **not a medical/agricultural diagnosis system**.

Color ratios alone cannot reliably identify a plant disease.

The output should be treated as a visual-analysis demo only.

## Original AI implementation

The repository also contains the original AI pipeline built around:

- FastAPI
- Streamlit
- Groq API
- a Llama vision model
- image upload and base64 conversion
- structured AI response parsing

That mode requires a valid:

```text
GROQ_API_KEY
```

Do not commit a real API key to GitHub.

## Project structure

```text
Advance-leaf-disease-detection/
│
├── app.py
├── main.py
├── Leaf Disease/
├── Media/
├── requirements.txt
├── test_api.py
├── utils.py
├── vercel.json
│
└── web/
    └── index.html
```

## Run the live-style web demo locally

No Python setup is needed.

```bash
cd web
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Run the original FastAPI version

Create a virtual environment and install dependencies:

```bash
pip install -r requirements.txt
```

Set the Groq key in your environment:

### Windows PowerShell

```powershell
$env:GROQ_API_KEY="your_key_here"
```

### macOS / Linux

```bash
export GROQ_API_KEY="your_key_here"
```

Start the API:

```bash
uvicorn app:app --reload --port 8000
```

Swagger:

```text
http://127.0.0.1:8000/docs
```

## Run the original Streamlit UI

```bash
streamlit run main.py
```

## Technology

### Hosted demo
- HTML
- CSS
- JavaScript
- Canvas image processing
- Vercel

### Original AI version
- Python
- FastAPI
- Streamlit
- Groq API
- Llama vision model

## Why there are two modes

The full AI version depends on a private external API key.

For a public portfolio link, the no-key browser demo is more reliable because:

- it opens immediately,
- no secret is exposed,
- no paid/private credential is required,
- reviewers can still interact with a real image-processing workflow.

The original AI source remains in the repository so the full architecture is still available.

## Author

**Sankalp Gupta**

- GitHub: https://github.com/Sankalp-gupta1
- LinkedIn: https://www.linkedin.com/in/sankalp-gupta-rishi-8617302b0/
