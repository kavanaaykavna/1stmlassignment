# memo-bot – Build Log

## Project Information

**Project:** memo-bot  
**Checkpoint:** Build (Core) – MVP

---

# Objective

Build a memory-based AI assistant that remembers previous conversations, retrieves user context, and generates intelligent responses using a live AI model. The application should complete the conversation flow end-to-end while storing conversation history for future interactions.

---

# Original MVP Specification

The planned MVP included:

- Flask web application
- Interactive chat interface
- AI-powered responses
- Persistent memory
- Context-aware conversations
- Responsive UI
- End-to-end workflow without manual intervention

---

# Build Log

## Day 1

### Goal
Set up the Flask application and build the basic chatbot interface.

### Completed
- Created the Flask application (`app.py`)
- Designed the frontend using HTML, CSS, and JavaScript
- Connected the frontend with the Flask backend
- Organized the project into `templates`, `static`, `services`, and `memory` directories

### Issue
The application failed to load the HTML page.

### Cause
The `index.html` file was not placed inside the `templates` directory required by Flask.

### Fix
Moved the HTML file into the `templates` folder and updated the Flask routing configuration.

**Status:** ✅ Completed

---

## Day 2

### Goal
Fix message sending functionality.

### Issue
Messages were not being sent when the Send button was clicked.

### Cause
The browser was not triggering the form submission correctly.

### Fix
- Replaced the form submission with a JavaScript click handler.
- Added Enter key support for sending messages.

**Status:** ✅ Completed

---

### Goal
Add the ability to start a new conversation.

### Issue
Users had no way to clear the existing conversation.

### Fix
- Added a reset endpoint.
- Added a **New Chat** button that clears the current session memory.

**Status:** ✅ Completed

---

## Day 3

### Goal
Integrate an AI model.

### Initial Plan
Use Google's Gemini API.

### Issue
Gemini's free-tier daily quota was exhausted during development.

### Result
Every API request failed, preventing reliable testing.

### Fix
Added proper exception handling so quota errors returned a friendly message instead of crashing the application.

**Status:** ✅ Completed

---

### Goal
Switch AI provider.

### Issue
Gemini's quota frequently interrupted testing and development.

### Fix
- Added `groq_service.py`
- Created `ai_router.py`
- Implemented provider routing using an environment variable
- Switched the application to Groq for reliable development and testing

**Status:** ✅ Completed

---

## Day 4

### Goal
Implement persistent memory.

### Completed
- Created `memory_service.py`
- Added memory loading
- Added memory saving
- Stored conversations inside `memory/memory.json`

### Issue
Conversation history disappeared after restarting the application.

### Cause
Memory was stored only temporarily during runtime.

### Fix
Saved every conversation automatically into `memory/memory.json`.

**Status:** ✅ Completed

---

### Goal
Fix shared-memory issue before deployment.

### Issue
All visitors shared one global conversation because the same `memory.json` file was used for every user.

### Fix
Updated the memory system to store conversations separately using unique session IDs.

**Status:** ✅ Completed

---

## Day 5

### Goal
Generate context-aware AI responses.

### Issue
The chatbot ignored previous conversations.

### Cause
Only the latest user message was being sent to the AI model.

### Fix
Retrieved conversation history before every request and included it in the prompt sent to the AI model.

**Status:** ✅ Completed

---

### Goal
Improve prompt handling.

### Completed
- Added `prompt_service.py`
- Centralized prompt creation
- Improved response quality and conversation consistency

**Status:** ✅ Completed

---

## Day 6

### Goal
Improve the user interface.

### Completed
- Redesigned the chat layout
- Added loading animation
- Improved spacing and alignment
- Added automatic scrolling
- Improved responsiveness
- Enhanced the overall user experience

**Status:** ✅ Completed

---

### Goal
Prepare the application for deployment.

### Issue
The project was configured only for local development.

### Fix
- Updated `requirements.txt`
- Added a `Procfile`
- Configured Flask to use dynamic host and port values
- Verified deployment compatibility

**Status:** ✅ Completed

---

# Final Project Structure

```text
memo-bot/

│── app.py
│── Procfile
│── requirements.txt
│── .env
│── .gitignore
│
├── memory/
│   └── memory.json
│
├── services/
│   ├── ai_router.py
│   ├── gemini_service.py
│   ├── groq_service.py
│   ├── memory_service.py
│   └── prompt_service.py
│
├── static/
│   ├── script.js
│   └── style.css
│
├── templates/
│   └── index.html
│
└── venv/
```

---

# Live Connections Used

## Groq API

**Purpose:** Generate intelligent conversational responses.

**Status:** ✅ Connected

---

## Local Memory (`memory/memory.json`)

**Purpose:** Persist conversation history between sessions.

**Status:** ✅ Connected

---

# Final Architecture

```text
User
   │
   ▼
Frontend (HTML / CSS / JavaScript)
   │
   ▼
Flask Backend (app.py)
   │
   ▼
ai_router.py
   │
   ├────────────► groq_service.py
   │                  │
   │                  ▼
   │              Groq API
   │
   └────────────► memory_service.py
                      │
                      ▼
             memory/memory.json
```

---

# Features Completed

- Flask backend
- Responsive chat interface
- Groq API integration
- AI provider routing
- Persistent memory
- Session-based conversation storage
- Prompt management
- Automatic conversation saving
- Automatic memory retrieval
- New Chat functionality
- End-to-end conversational workflow

---

# Features Deferred

### Voice Assistant

**Reason:** Outside the scope of the MVP.

---

### User Authentication

**Reason:** Session-based memory is sufficient for the current version.

---

### Cloud Database

**Reason:** Local JSON storage satisfies the MVP requirements.

---

### Calendar Integration

**Reason:** Planned for a future version.

---

# Challenges Faced

- Flask routing issues
- JavaScript event handling
- Gemini API quota limitations
- Switching AI providers
- Prompt engineering
- Persistent memory implementation
- Session management
- Deployment configuration

Each issue was resolved during development and documented in this build log.

---

# Final MVP

The **memo-bot** application successfully:

- Accepts user messages
- Retrieves previous conversation history
- Generates contextual responses using the Groq API
- Stores conversations automatically
- Maintains session-specific memory
- Allows users to start new conversations
- Completes the full workflow without manual intervention

---

# Deliverables

- ✅ Working memo-bot application
- ✅ Groq API integration
- ✅ Persistent memory system
- ✅ Responsive chat interface
- ✅ Build log
- ✅ GitHub repository
- ✅ Raw end-to-end demonstration video

---

# Project Status

**Checkpoint 1 – Build (Core MVP): COMPLETED ✅**
