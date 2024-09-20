# Bilingual Interactive Voice Chatbot (Arabic/French)

## Description

This project is an interactive voice-activated chatbot capable of understanding and responding in both Arabic and French. Using **ChatterBot**, the chatbot generates dynamic responses to user input. It listens for voice commands using **speech recognition** and responds via **text-to-speech (TTS)**. Users can engage with the chatbot entirely through voice, allowing for a seamless hands-free experience.

### Key Features
- **Bilingual Interaction**: The chatbot supports both Arabic and French languages. Users can choose their preferred language at the beginning of the conversation.
- **Voice Commands**: The system continuously listens for a specific trigger word to activate the chatbot and accepts voice commands from users.
- **Natural Audio Responses**: The chatbot provides responses in the form of synthesized speech, making the interaction more natural and user-friendly.
- **Dynamic Conversations**: The chatbot can handle various queries using ChatterBot's machine learning-based response generation.
- **Trigger Word Activation**: The chatbot is activated by specific trigger words, allowing users to interact without needing a graphical interface.

## Technologies Used
- **Flask**: Serves the web application and handles WebSocket connections.
- **ChatterBot**: Provides the chatbot's machine learning capabilities for generating responses.
- **SpeechRecognition**: Captures and processes audio input from users.
- **Pyt2s (Text-to-Speech)**: Converts chatbot responses into synthesized speech.
- **Pydub**: Handles audio playback.
- **Sounddevice**: Records audio from the user for speech recognition.
- **FuzzyWuzzy**: Used to detect trigger words with some tolerance for variations in pronunciation.

## Installation and Setup

### Prerequisites
- Python 3.x
- Required libraries (listed in `requirements.txt`)

### Installation Steps

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/bilingual-chatbot.git
    cd bilingual-chatbot
    ```

2. **Install dependencies**:
    You can install the required packages by running:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the application**:
    Run the main script to start the chatbot system:
    ```bash
    python app.py
    ```

4. **Access the chatbot**:
    Once the app is running, it will start listening for trigger words and responding to voice commands. You can access the status via `localhost:5000`.

## Usage

### Interacting with the Chatbot
1. The system waits for a trigger word (e.g., "عُرِيف" or "Orriif").
2. Once activated, the chatbot asks for your language preference: Arabic or French.
3. After selecting the language, ask questions or give commands in that language.
4. The chatbot will process your query and respond with synthesized speech.
5. Say an exit phrase (e.g., "إلى اللقاء" or "Au revoir") to end the conversation and return the system to standby mode.

### Customizing Trigger Words
You can modify the list of trigger words in the `is_trigger_word_in_text()` function located in `app.py`.

### Customizing Responses
To customize the responses or logic of the chatbot, modify the **ChatterBot** logic adapters defined in `app.py`.

## Project Structure
```bash
.
├── app.py               # Main application file
├── requirements.txt      # Python dependencies
├── README.md             # This README file
└── database.sqlite3      # Chatbot's knowledge base (SQLite database)
