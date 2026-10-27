MIYORA MD — Vercel frontend

Files:
- index.html / main.html: home page
- pair.html: WhatsApp pairing page
- settings.html: bot settings
- react.html: channel react panel
- admin.html: admin panel
- vercel.json: proxies /code and /code/* requests to the Heroku backend

Deploy:
1. Extract this ZIP.
2. Upload the folder/repository to GitHub.
3. In Vercel choose Add New Project and import that repository.
4. Framework Preset: Other. Build Command: leave empty. Output Directory: . (root).
5. Deploy.

Important:
- Backend URL configured: https://fandenda-ed1feea7ee4a.herokuapp.com
- The Heroku backend must actually expose /code, /code/api/* endpoints and allow the required requests.
- This frontend proxy does not create missing backend routes or fix a sleeping/crashed bot.
- Test /pair.html first. If pairing fails, inspect Heroku logs and confirm the backend's /code?number=... route returns JSON.
- Admin page uses the backend's /code/api/admin endpoints; it cannot bypass backend authentication.
