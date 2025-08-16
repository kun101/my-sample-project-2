# Local Quick Start (Linux/WSL)
Run this FastAPI project on Linux/WSL as follows:
## Virtual Environment Setup [First Time Only]
1) Create the virtual environment `python3 -m venv venv`
2) Load the virtual environment `source venv/bin/activate`
3) Install Command: `pip install -r requirements.txt`

## Run Server
1) Load the virtual environment `source venv/bin/activate`
2) Set the `OPENAI_API_KEY` and `OPENAI_ADMIN_KEY` environment variables. Eg. `export OPENAI_API_KEY=<YOUR_KEY>`
3) Run `python load_env.py`
4) Start Command: `uvicorn main:app --host 127.0.0.1 --port 8001`

# Host on Render
1) Push your code to a public GitHub Repository
2) Go to [https://render.com](https://render.com/)
3) Login using your GitHub Account
4) Create a Web Service
5) Link your repository to the project
6) Enter the Install Command as : `pip install -r requirements.txt`
7) Enter the Start Command as : `uvicorn main:app --host 0.0.0.0 --port $PORT`
8) Set the `OPENAI_API_KEY` and `OPENAI_ADMIN_KEY` environment variables.
9) Deploy