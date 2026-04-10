# Meeting Notes Assistant Demo

This repository contains a simple demo application that uses LangChain with Google Gemini (via `langchain-google-genai`) to analyze a meeting transcript and support follow-up questions in the same session.

## Project Structure

- `main.py` - Main demo script that loads a transcript, creates an agent, and runs an interactive prompt loop.
- `encoding.py` - Helper module to read `transcript.txt` using multiple character encodings.
- `transcript.txt` - Example meeting transcript used as the input for analysis.
- `requirements.txt` - Python package dependencies.
- `.env` - Environment variables for API credentials (not included in source control).

## Features

- Loads and analyzes a meeting transcript.
- Uses `ChatGoogleGenerativeAI` as the underlying model.
- Provides follow-up question handling in a persistent session.
- Extracts key points, action items, and summaries based on transcript content.
- Stores agent state in memory using `InMemorySaver`.

## Requirements

- Python 3.11 or later
- A Google Generative AI API key configured in `.env`

## Setup

1. Create and activate a virtual environment:

   ```bash
   python -m venv venv
   .\venv\Scripts\activate
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file in the project root with your Google API credentials. For example:

   ```bash
   GOOGLE_API_KEY=your_api_key_here
   ```

4. Ensure `transcript.txt` contains the meeting text you want the agent to analyze.

## Running the Demo

Run the main script:

```bash
python main.py
```

The script will:

1. Load the meeting transcript.
2. Analyze it with the agent.
3. Enter an interactive loop where you can ask follow-up questions.

Type `exit` to quit.

## Notes

- The current `main.py` example demonstrates an initial transcript analysis followed by user-driven follow-up queries.
- `encoding.py` ensures the transcript file is read correctly even if it uses a non-UTF-8 encoding.

## License

This project is provided as a demo and has no license specified.
