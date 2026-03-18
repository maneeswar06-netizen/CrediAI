# CrediAI – Vercel entry

This folder is a **redirect** to the real CrediAI app (hosted on Render).

- **Deploy on Vercel:** Connect this repo, set **Root Directory** to `vercel-app`, then deploy.
- Your Vercel URL (e.g. `credi-ai.vercel.app`) will show a short “Loading…” then open https://crediai.onrender.com.
- The actual Streamlit app runs on Render; Vercel only serves this redirect page.

## Deploy steps

1. Go to [vercel.com](https://vercel.com) and sign in (e.g. with GitHub).
2. **Add New** → **Project** → import **maneeswar06-netizen/CrediAI**.
3. **Important:** Set **Root Directory** to `vercel-app`:
   - Click **Edit** next to "Root Directory"
   - Enter **vercel-app** (no trailing slash)
   - Confirm so only the redirect app is built, not the Python/Streamlit app.
4. Click **Deploy**.
5. Your app will be at `https://your-project.vercel.app`.

If you see *"No python entrypoint found"*, the root is wrong: Vercel is building the whole repo. Set Root Directory to **vercel-app** and redeploy.

## APK

After deployment, set the Android app URL to your Vercel URL in  
`android-app/app/src/main/res/values/strings.xml` → `credi_app_url`,  
so the APK opens Vercel, which then redirects to Render.
