# Groq Streamlit Chat (Open Source)

Minimal Streamlit chat application using the Groq Python SDK with streaming responses.

## What you get
- Streamlit app (`app.py`) that connects to Groq's Chat Completions API and streams responses.
- Uses Streamlit `session_state` to maintain conversation history.
- Example `requirements.txt` and deployment instructions.

## How to run locally
1. Create a Python 3.10+ virtualenv and activate it.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set your Groq API key in the environment:
   ```bash
   export GROQ_API_KEY="your_api_key_here"
   ```
   Or create `.streamlit/secrets.toml` with:
   ```
   GROQ_API_KEY = "your_api_key_here"
   ```
4. Run:
   ```bash
   streamlit run app.py
   ```

## Deploy to Streamlit Community Cloud (Streamlit Cloud)
1. Create a public GitHub repository and push these project files.
2. Login at https://share.streamlit.io with your GitHub account.
3. Click **Create app**, pick the repository, branch, and `app.py` file, then **Deploy**.
4. Add the `GROQ_API_KEY` to your app's Secrets (Settings → Secrets) on Streamlit Cloud. Do **not** hardcode the key.

## Notes & Caveats
- This example uses Groq's streaming API. Streaming yields partial deltas; the code attempts to handle a few delta shapes but may need slight adjustment if Groq changes the payload format.
- The app is intentionally minimal for quick deployment. You can extend it with message roles, RAG, or file upload.

## License
MIT
