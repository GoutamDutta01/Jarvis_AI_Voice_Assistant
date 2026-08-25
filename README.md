# Jarvis Mark 2

Jarvis Mark 2 is a Python-based voice assistant and desktop AI app that combines speech recognition, natural-language responses, real-time web search, app automation, text-to-speech, and a custom graphical interface.

## Overview

This project uses:
- PyQt5 for the desktop GUI
- Python speech recognition for voice input
- Groq and Cohere APIs for AI reasoning and response generation
- Google/Youtube integration for search and playback
- App opening/closing automation via system commands
- Local file-backed chat logs and interface state data

## Project structure

- `Backend/` – AI logic, search, automation, and speech processing modules
- `Frontend/` – PyQt GUI, graphics, and runtime data files used by the interface
- `Data/` – chat logs and generated audio/HTML artifacts
- `Main.py` – application entry point
- `Requirements.txt` – Python dependencies
- `.env` – local environment variables containing API keys and user settings

## Features

- Voice-driven assistant interaction
- Chatbot responses with Groq-based LLM support
- Real-time search answer generation
- Google and YouTube search commands
- Open/close application commands
- System controls such as volume and playback actions
- Content generation and image-generation workflows
- Persistent conversation history stored in `Data/ChatLog.json`

## Requirements

- Python 3.10+
- pip package manager
- Access to the required API keys in a local `.env` file

## Setup

1. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```

2. Install dependencies:
   ```bash
   pip install -r Requirements.txt
   ```

3. Create a `.env` file in the project root with the required values:
   ```env
   Username=YourName
   Assistantname=Jarvis
   GroqAPIKey=your_groq_key
   CohereAPIKey=your_cohere_key
   HuggingFaceAPIKey=your_huggingface_key
   InputLanguage=en
   AssistantVoice=en-CA-LiamNeural
   ```

4. Run the app:
   ```bash
   python Main.py
   ```

## Notes

- The `.env` file contains secrets and should never be committed to version control.
- Runtime-generated files under `Frontend/Files/` and `Data/` are intentionally excluded in the repository ignore list.
- Some features depend on external services and system-level tools, so availability may vary by platform and environment.

## Common runtime artifacts

The project creates temporary conversation, status, and media files at runtime, including:
- `Frontend/Files/*.data`
- `Data/ChatLog.json`
- `Data/speech.mp3`
- `Data/Voice.html`

These should be treated as local development output rather than source files.
