# Emobuddy
Emobuddy is an AI chatbot that detects emotions from user input and responds with appropriate emotional tone and empathy. Using transformers for sentiment analysis, it integrates with a Flask API to store and retrieve conversations, making it ideal for emotional support systems and analyzing emotional trends.
**Emobuddy: Emotional Support AI Chatbot**
**Overview**
Emobuddy is an AI-powered chatbot designed to provide real-time emotional support using NLP-based emotion detection models. The chatbot analyzes user input, detects emotions, and responds accordingly to enhance the user experience, making it ideal for emotional well-being and mental health applications.

**Features**
Emotion detection using multiple AI models
Conversational responses tailored to detected emotions
Real-time chat functionality
SQLite database for storing conversations
Frontend built with HTML, CSS, and JavaScript
Backend powered by Flask
**Project Structure**
/project
├── backend/
│   ├── server.py          # Main Flask server
│   ├── emotion_detection.py  # Emotion detection logic
│   ├── chatbot.db         # SQLite database
│   ├── requirements.txt   # Dependencies
│
├── frontend/
│   ├── index.html         # Chat UI
│   ├── style.css          # Styles
│   ├── script.js          # Frontend logic
│
└── README.md              # Project documentation
**Installation**
1. Clone the repository
bash
Copy
Edit
git clone https://github.com/Kamali-13/Emobuddy.git
cd emotional-support-chatbot
2. Install dependencies
Make sure you have Python installed and set up a virtual environment.

bash
Copy
Edit
pip install -r backend/requirements.txt
3. Set up the database
Run the following command to initialize the SQLite database:

bash
Copy
Edit
python -c "import sqlite3; sqlite3.connect('backend/chatbot.db').close()"
4. Run the backend
Start the Flask server by running:

bash
Copy
Edit
python backend/server.py
The Flask server should now be running at http://127.0.0.1:5000/.

5. Run the frontend
Open frontend/index.html in a browser or use Live Server in VS Code to run the chat UI.

**API Endpoints**
POST /chat
Description: Process user input and return an appropriate chatbot response.

**Request Body:**
json
{
  "user_input": "I feel sad today."
}
**Response:**
json

{
  "response": "I'm here for you. Want to talk about it?",
  "emotion": "sadness",
  "score": 0.87,
  "tone": "negative"
}
**Future Enhancements**
Improve chatbot response accuracy using GPT-based models.
Implement voice support for accessibility.
