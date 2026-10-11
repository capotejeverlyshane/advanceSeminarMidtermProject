# VISTA (Virtual Intelligent Smart Technical Assistant)

## Project Overview
VISTA is an AI-powered Citizen's Charter and Campus Inquiry Assistant designed to provide automated, accurate responses to institutional inquiries, complaints, and student services.

## Architecture
- **Frontend** (`/frontend`):
  - Stack: HTML5, CSS3, Vanilla JavaScript.
  - Port: `8085` (served via `npx http-server`).
  - Key Pages: `index.html` (Citizen Chat Portal), `admin.html` (Administrative Analytics Dashboard).
- **Backend** (`/backend`):
  - Framework: FastAPI (Python 3.10+).
  - Port: `8000` (run via `uvicorn app:app --reload`).
  - NLP Engine: Scikit-learn intent classifier trained on `data/answers.json`.
  - Database: Supabase PostgreSQL integration (`supabase_client.py`).

## Running the Application
To run the full stack:
1. Double-click or execute `start_vista.bat` in the root folder, or:
2. **Backend**:
   ```bash
   cd backend
   .venv\Scripts\activate
   uvicorn app:app --reload --port 8000
