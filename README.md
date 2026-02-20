# SpeakSync
Real-time presentation coach designed to bridge the gap between solo practice and professional delivery. While effective communication is a vital skill, practicing alone often leads to overlooking crucial elements like posture and composure. This application provides a "second pair of eyes and ears" to ensure every rehearsal counts.

🚀 Getting Started
Prerequisites
Python installed on your machine.

An OpenAI API Key.

A free Stream account.

Installation

Install the uv package manager:

Bash

## For Windows
`powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"`

## For Linux/MacOS
`curl -LsSf https://astral.sh/uv/install.sh | sh`

Initialize the project and virtual environment:

Bash

uv init
uv venv

Install dependencies:

Bash

`uv add vision-agents [getstream, openai, ultralytics] python-dotenv`

Configuration

Create a .env file in the root directory and add your credentials:

Code snippet

STREAM_API_KEY=your-stream-api-key

STREAM_API_SECRET=your-stream-secret

OPENAI_API_KEY=your-openai-api-key

CALL_ID="practice-room"

###🏗️ Project Structure

Presentation Coach/
├── instructions/
│   └── coach.md          # Coaching philosophy and personality [cite: 137]
├── .env                  # API keys and secrets [cite: 132]
├── main.py               # The Central Processing Unit of the app [cite: 190]
├── download_yolo_pose.py # Utility to download the YOLO11 model [cite: 138]
└── pyproject.toml        # Project dependencies [cite: 151]

###🎮 Usage
Download the Vision Model:
Run the utility script to fetch the yolo11n-pose.pt model file.

Bash
`python download_yolo_pose.py`

Launch the Coach:
Run the main application. The agent will join the call, greet you, and start monitoring your performance automatically.

Bash
`python main.py`

###📜 Coaching Philosophy
The agent's personality is defined in instructions/coach.md. It is designed to be encouraging and focused on specific metrics like pace, clarity, and posture to ensure you stay relaxed yet professional during your practice.


Based on the tutorial by Timothy Olanrewaju via freeCodeCamp.
