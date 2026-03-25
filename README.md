# Decisio — Decision Engine 🧠✨

A smart decision-making web app powered by Groq's free AI API, deployed on Vercel's free tier.

---

## 🚀 Deploy in 5 Steps

### Step 1 — Get your free Groq API key
1. Go to [console.groq.com](https://console.groq.com)
2. Sign up (free, no credit card needed)
3. Go to **API Keys** → click **Create API Key**
4. Copy the key and save it somewhere safe

---

### Step 2 — Put the project on GitHub
1. Go to [github.com](https://github.com) and create a new repository (e.g. `decision-engine`)
2. Upload these 3 files maintaining the folder structure:
   ```
   index.html
   api/analyze.js
   ```
   > Make sure `analyze.js` is inside a folder called `api`

---

### Step 3 — Connect to Vercel
1. Go to [vercel.com](https://vercel.com) and sign up / log in (free)
2. Click **Add New Project**
3. Select your GitHub repo (`decision-engine`)
4. Click **Deploy** — don't change any settings

---

### Step 4 — Add your Groq API key to Vercel
1. After deploy, go to your project dashboard on Vercel
2. Click **Settings** → **Environment Variables**
3. Add a new variable:
   - **Name:** `GROQ_API_KEY`
   - **Value:** paste your Groq key here
4. Click **Save**

---

### Step 5 — Redeploy
1. Go to **Deployments** tab in Vercel
2. Click the three dots on the latest deployment → **Redeploy**
3. Wait ~30 seconds — done! ✅

Your site is now live at `https://your-project-name.vercel.app` 🎉

---

## 📁 File Structure
```
decision-engine/
├── index.html        ← the full frontend UI
└── api/
    └── analyze.js    ← serverless proxy (keeps API key safe)
```

---

## 💡 How It Works
- The frontend (`index.html`) sends the decision prompt to `/api/analyze`
- The serverless function (`api/analyze.js`) forwards it to Groq using the secret API key
- Groq returns the AI analysis, which the frontend renders into cards
- Your API key is **never exposed** in the browser

---

## 🆓 Cost
- **Vercel Hobby tier:** Free (100k function calls/month)
- **Groq API:** Free tier with generous rate limits
- **Total cost: $0**
