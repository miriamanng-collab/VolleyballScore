# Volleyball Score

Score keeper with serve rotation, saved teams, match history, standings and live sync between devices using a league code (no accounts needed).

## 1. Create the free sync database (Firebase, ~5 minutes)
1. Go to https://console.firebase.google.com and create a project (Analytics not needed).
2. **Build → Firestore Database → Create database** (production mode, any region).
3. Open the **Rules** tab, paste the contents of `firestore.rules`, and **Publish**.
4. **Project settings (gear icon) → Your apps → Web (`</>`)**, register an app, and copy the `firebaseConfig` values.
5. Paste them into `config.js`.

## 2. Publish on GitHub Pages
1. Create a GitHub repository and upload every file in this folder (keep them in the root).
2. **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder `/ (root)`. Save.
3. After a minute your site is live at `https://<your-username>.github.io/<repo-name>/`.

## 3. Use it
- On the home page, tap **Start a new league** and share the code shown with your other devices.
- On each other device open the site, enter the code under **Join a league**.
- Install on a phone: iPhone Safari → Share → Add to Home Screen; Android Chrome → menu → Install app.

## Notes
- Anyone who knows a league code can read and edit that league, so treat it like a password. Codes from "Start a new league" are 8 random characters.
- Firebase's free tier is far more than a league needs.
- The app also works without Firebase configured; data then stays on that device only.

## Before uploading: replace the placeholders
Search all files for `YOUR-USERNAME` and `YOUR-REPO` and replace them with your GitHub username and repository name. They appear in `index.html` (canonical and social tags), `robots.txt` and `sitemap.xml`.
