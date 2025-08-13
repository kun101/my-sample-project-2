# TDS Project 2 - Render Deployment Guide

## Quick Deploy to Render

### Option 1: Using render.yaml (Recommended)
1. Push your code to GitHub
2. Connect your GitHub repository to Render
3. Render will automatically detect the `render.yaml` file
4. Set the environment variables in Render dashboard:
   - `GENAI_API_KEY`: Your Google AI API key
   - `NGROK_AUTHTOKEN`: Your ngrok auth token (optional for Render deployment)

### Option 2: Manual Setup
1. Create a new Web Service on Render
2. Connect your GitHub repository
3. Configure the service:
   - **Environment**: Python 3
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `uvicorn main:app --host 0.0.0.0 --port $PORT`
   - **Instance Type**: Free (or paid if needed)

### Environment Variables Required:
- `GENAI_API_KEY`: Get from https://aistudio.google.com/apikey
- `NGROK_AUTHTOKEN`: Get from https://ngrok.com/ (optional for Render)

### Local Development:
```bash
# Install dependencies
pip install -r requirements.txt

# Run locally
python main.py
# OR
uvicorn main:app --reload
```

### Features:
- FastAPI backend with HTML frontend
- File upload and processing
- LLM integration with Google Gemini
- Data analysis and visualization
- Automatic code generation and execution

### File Structure:
- `main.py`: FastAPI application
- `task_engine.py`: Code execution engine
- `gemini.py`: LLM integration
- `frontend.html`: Web interface
- `requirements.txt`: Python dependencies
- `Procfile`: Render deployment configuration
- `render.yaml`: Render service configuration
