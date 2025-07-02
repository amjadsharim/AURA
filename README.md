
AURA (Adaptive User-Responsive Assistant)
=========================================

AURA is a behavior-aware, AI-powered voice assistant designed to enhance accessibility for blind and visually impaired users. 
It integrates Large Language Models (LLMs) like GPT-4 with real-time user behavior tracking to dynamically adapt speech rate, verbosity, and language complexity.

-----------------------------------------
Key Features
-----------------------------------------
- Voice input and output (speech recognition + text-to-speech)
- Real-time user profiling based on behavior (replay, skip, duration)
- Personalized prompt generation using LLM (e.g., GPT-4)
- Closed-loop feedback system to improve usability per session
- Interaction logging and adaptive user profile updates
- Cross-platform compatibility: Windows, macOS, Linux

-----------------------------------------
Project Structure
-----------------------------------------
adaptive_voice_assistant/
│
├── main.py                         # Entry point: orchestrates assistant logic
├── config.json                     # Default configuration (optional)
├── user_profiles/                  # Stores dynamic user settings (JSON)
│   └── blind_user_001.json         
├── logs/                           # Logs interaction behavior
│   └── interaction_log.csv
├── modules/                        # Modular assistant logic
│   ├── speech_input.py             # Speech-to-text module
│   ├── speech_output.py            # Text-to-speech module
│   ├── behavior_logger.py          # Logs behavior vectors
│   ├── profile_manager.py          # Loads, saves, adapts user profiles
│   ├── prompt_generator.py         # Builds adaptive prompts
│   ├── llm_interface.py            # Interfaces with GPT-4/3.5

-----------------------------------------
How to Run
-----------------------------------------
1. Install Python 3.9+:
   - https://www.python.org/downloads 
   - Ensure “Add Python to PATH” is checked

2. Unzip the project folder.

3. Install Required Libraries:
   pip install openai speechrecognition pyttsx3 pyaudio

   If pyaudio fails:
   pip install pipwin
   pipwin install pyaudio

4. Set your OpenAI API key in main.py:
   openai.api_key = "sk-XXXXXXXXXXXXXXXXXXXXXXXX"

5. Run:
   python main.py

-----------------------------------------
Behavior Logging & Adaptation
-----------------------------------------
- Replay-dominant users → slower speech, simpler answers
- Skip-dominant users → faster speech, concise answers
- Logs: user_profiles/ and logs/interaction_log.csv

-----------------------------------------
Technologies
-----------------------------------------
- Python 3.9+
- OpenAI GPT-4 or GPT-3.5
- pyttsx3, SpeechRecognition
- JSON, CSV

-----------------------------------------
Contact
-----------------------------------------
Amjad Ali
Department of Computer Science, University of Peshawar
Email: amjad.cs@uop.edu.pk
