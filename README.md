# Neon City RPG 🎲

Neon City RPG is an immersive, voice-driven cyberpunk adventure. Users take on the role of a protagonist in a gritty, high-tech future, interacting with an AI "Game Master" (GM) through natural speech. The GM narrates the world, reacts to player choices, and drives a dynamic plot based on continuous session history.

## 🚀 Features

* **Atmospheric AI Game Master**: Powered by **Google Gemini 2.0 Flash**, the GM provides noir-style, atmospheric narration and reacts dynamically to any player action.
* **Voice-to-Voice Gameplay**: Integrates **AssemblyAI** for transcribing player speech and **Murf AI** (using a dramatic "Promo" style voice) for the GM's narration.
* **Persistent Story History**: The system maintains the full conversation history during a session, ensuring plot continuity and contextual awareness for every turn.
* **Immersive Cyberpunk UI**: A dedicated "Neon City" interface featuring a dark aesthetic, neon glow effects, and a live story log.
* **Dynamic Plot Progression**: A mini-arc structure that guides players through escaping surveillance drones, finding contacts, and decrypting mysterious data chips.

## 🛠️ Tech Stack

### Backend

* **Framework**: FastAPI.
* **LLM**: Google Gemini 2.0 Flash (Game Master logic).
* **STT**: AssemblyAI (Player action transcription).
* **TTS**: Murf AI (GM voice generation with dramatic flair).
* **Environment Management**: `python-dotenv`.

### Frontend

* **Styling**: Tailwind CSS with custom cyberpunk themes and Google Fonts (Orbitron & Rajdhani).
* **Interactions**: Vanilla JavaScript with Axios for API communication.
* **Audio**: Web MediaRecorder API for capturing player voice input.

## 📂 Project Structure

```text
├── backend/
│   ├── main.py             # FastAPI app initialization & CORS setup
│   ├── routes.py           # GM logic, STT/TTS integration, & session handling
│   └── requirement.txt     # Python dependencies
├── frontend/
│   ├── index.html          # Cyberpunk-themed game window
│   ├── index.js            # Voice recording logic & history management
│   └── package.json        # Frontend dependencies
└── .env                    # API keys (Google, AssemblyAI, Murf)

```

## ⚙️ Setup & Installation

### Backend

1. Navigate to the `backend` directory.
2. Install the required Python packages:
```bash
pip install -r requirement.txt

```


3. Create a `.env` file and add your API keys:
```text
GOOGLE_API_KEY=your_gemini_key
ASSEMBLYAI_API_KEY=your_assemblyai_key
MURF_AI_API_KEY=your_murf_key

```


4. Launch the server:
```bash
python main.py

```



### Frontend

1. Navigate to the `frontend` directory.
2. Install dependencies:
```bash
npm install

```


3. Open `index.html` via a local development server (e.g., Live Server in VS Code).

## 📖 How to Play

1. **Enter Simulation**: Click "ENTER SIMULATION" to initialize the neural link and receive your opening scene from the GM.
2. **Speak Your Action**: Click and hold the microphone icon to record your action (e.g., "I try to hide behind the crates").
3. **Listen & React**: The GM will describe the outcome of your action and ask, "What do you do?" to keep the story moving.
4. **Reboot**: Use the "Reboot System" button at any time to clear the neural link and start a new adventure.
