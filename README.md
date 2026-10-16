# Smart Document Assistant

A Streamlit document-search app that accepts PDF, DOCX and TXT files and retrieves relevant passages using TF-IDF. No OpenAI, Groq, or other AI API key is required.

## Features
- Upload multiple PDF, DOCX and TXT files
- Search questions against relevant passages
- Display source file names and relevance scores
- Built-in fictional college FAQ sample
- Purple-themed Streamlit interface
- No external LLM API calls

## Deploy to Streamlit Community Cloud
1. Open https://share.streamlit.io/ and sign in with GitHub.
2. Choose **Create app**.
3. Repository: `pradeeppullamsetty/smart-document-assistant`
4. Branch: `main`
5. Main file path: `app.py`
6. Click **Deploy**. No secrets or API keys are required.

Streamlit will provide a public `https://....streamlit.app` URL after deployment succeeds.

## Run locally
```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install -r requirements.txt
py -m streamlit run app.py
```

## How it works
TF-IDF and cosine similarity retrieve relevant text passages. This version does not generate free-form LLM answers; it shows source text so users can verify information.

## Privacy
Do not upload confidential files to a public demo. Uploaded content is processed during the app session and is not sent to an external AI API.
