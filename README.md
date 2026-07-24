# GenerativeAI

A small generative AI demo project with chat, embedding, and movie information extraction examples using LangChain, Hugging Face, OpenAI, and Mistral AI.

## Prerequisites

- Python 3.10+ (recommended)
- Git (optional)
- A virtual environment for dependency isolation
- API keys for the service providers you want to use

## Install

From the project root:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install --upgrade pip
pip install -r requirements.txt
```

If you want to run the Streamlit apps, also install Streamlit:

```powershell
pip install streamlit
```

## Environment Variables

Create a `.env` file in the project root and add the keys required by the providers you use. Example:

```env
OPENAI_API_KEY=your-openai-api-key
HUGGINGFACEHUB_API_TOKEN=your-huggingface-token
MISTRALAI_API_KEY=your-mistralai-api-key
```

The project uses `python-dotenv`, so `.env` values are loaded automatically.

## Available Examples

### 1. `chatmodels/chat.py`

A minimal Mistral AI example that generates a poem.

```powershell
python chatmodels/chat.py
```

### 2. `chatmodels/chatbot.py`

A console-based mood chatbot with angry, funny, and sad modes.

```powershell
python chatmodels/chatbot.py
```

### 3. `chatmodels/UIchatbot.py`

A Streamlit mood-based chatbot UI.

```powershell
streamlit run chatmodels/UIchatbot.py
```

### 4. `CineSage/core.py`

A Hugging Face endpoint example that runs a simple chat prompt.

```powershell
python CineSage/core.py
```

### 5. `CineSage/UICore.py`

A Streamlit app that extracts structured movie data from text.

```powershell
streamlit run CineSage/UICore.py
```

### 6. `embeddingmodels/embeddings.py`

An OpenAI embeddings demo that generates vectors for sample text.

```powershell
python embeddingmodels/embeddings.py
```

## Notes

- The project does not currently include a single consolidated entrypoint.
- If a script fails because a provider key is missing, add the corresponding environment variable to `.env`.
- For Streamlit apps, use the browser URL shown in the terminal after `streamlit run`.

## Troubleshooting

- Ensure your virtual environment is activated.
- Confirm required packages are installed.
- Check that your `.env` file uses the correct provider variable names.
- If a script imports a package missing from `requirements.txt`, install it manually.

