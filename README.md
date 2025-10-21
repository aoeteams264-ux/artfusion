# ArtFusion — Ready repo for Render one-click deploy

## What this repo contains
- backend: FastAPI app with Replicate integration (placeholder if no token)
- frontend: React + Vite simple UI
- render.yaml for Render one-click deploy

## Quick steps
1. Create a new GitHub repo (e.g. aoeteams264-ux/artfusion) and push this project to it.
2. Go to https://render.com and click **New > Deploy from Git** and connect to your repo, or click the Deploy button if you use render.yaml.
3. In Render service settings for the backend, set environment variables:
   - REPLICATE_API_TOKEN (your token from replicate.com)
   - REPLICATE_MODEL_VERSION (model version id from replicate.com Versions tab)
4. Deploy and open the frontend URL Render provides.

## Local run (optional)
Backend:
```bash
cd backend/app
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```
Frontend:
```bash
cd frontend
npm install
npm run dev
```
