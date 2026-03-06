# 6:28 Zónázó Vonat 🚂

A fáradt, unott, de büszke 6:28-as zónázó vonat chatbotja.

## Railway Deployment

### 1. GitHub repo létrehozása
```bash
git init
git add .
git commit -m "6:28 zónázó indulás"
git remote add origin https://github.com/FELHASZNALONEVED/628-vonat.git
git push -u origin main
```

### 2. Railway projekt
1. Menj a [railway.app](https://railway.app) oldalra
2. **New Project → Deploy from GitHub repo**
3. Válaszd ki a repót

### 3. Environment variable beállítása
Railway dashboardon: **Variables** fül → **Add Variable**:
```
OPENAI_API_KEY = sk-...az_openai_api_kulcsod...
```

### 4. Kész!
Railway automatikusan buildeli és deploy-olja. Kapod az URL-t (pl. `628-vonat.up.railway.app`).

## Local futtatás

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
uvicorn main:app --reload
```

Majd nyisd meg: http://localhost:8000
