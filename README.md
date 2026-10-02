# CatCodeDidi Web Backend

This backend was created to support the CatCodeDidi web version by handling the server-side logic, AI requests, and API communication that the frontend needs.

## Why this project was created

The CatCodeDidi web version needs a reliable backend to:

- receive user prompts from the frontend
- send those prompts to Google's Gemini AI
- process the AI response
- return the result to the web application
- manage CORS and API endpoints for browser access

Without this backend, the web version would not be able to communicate with the AI assistant properly.

## Project purpose

This project acts as the backend layer for CatCodeDidi, allowing the web interface to interact with the AI assistant in a structured and scalable way.

## Tech stack

- Python
- FastAPI
- Gemini AI integration
- Python dotenv for environment configuration

## Main files

- `main.py` - FastAPI app and API routes
- `gemini_ai.py` - Gemini AI integration logic
- `requirements.txt` - Python dependencies

## API endpoint

### Home route

- GET `/`
- Returns a welcome message

### Prompt route

- POST `/Prompt`
- Accepts a JSON body like:

```json
{
  "Prompt": "Hello Didi"
}
```

The backend sends this prompt to Gemini and returns the AI response.

## Setup

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Create a `.env` file and add your Gemini API key:

```env
GEMINI_API_KEY=your_api_key_here
```

3. Run the server:

```bash
uvicorn main:app --reload
```

## Conclusion

This backend was created specifically for the CatCodeDidi web version so that the frontend can run smoothly while the AI assistant logic is handled in a secure and efficient backend environment.
