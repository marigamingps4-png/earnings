# Earnings app (installable)

Files: index.html, manifest.webmanifest, sw.js, icon-*.png. No build step.

## 1. Put the app on GitHub Pages (repo: earnings)
1. Open your `earnings` repo on github.com > Add file > Upload files. Drag in ALL the files from this folder (not the folder itself). Commit.
2. Repo > Settings > Pages > Deploy from a branch > `main` / root > Save.
3. After a minute your app is at https://YOUR-USERNAME.github.io/earnings/

Note: on a free GitHub account, Pages needs a PUBLIC repo. The app code has no personal data, so that is fine. Keep your DATA in a separate PRIVATE repo (step 2).

## 2. Your data repo (private)
1. Create a new PRIVATE repo, e.g. `earnings-data` (tick "Add a README").
2. github.com > Settings > Developer settings > Personal access tokens > Fine-grained tokens > Generate.
   - Repository access: Only select repositories > earnings-data
   - Permissions > Repository > Contents: Read and write
   - Copy the token.

## 3. Connect the app
Open the app > Settings > GitHub sync:
- GitHub username: yours
- Repository: earnings-data
- Data file: earnings-data.json
- Branch: main
- Access token: paste it
Tap "Save to GitHub now". Your data is now a file in your repo. It saves ~3 seconds after each change and loads when you open the app.

## 4. Install on your phone
- Android (Chrome): menu > Install app / Add to Home screen.
- iPhone (Safari): Share > Add to Home Screen.

## Move your current data
In the old claude.ai version: Settings > Backup > "Show my data", copy the text.
In the installed app: Settings > Backup > paste > "Import pasted data".

## Notes
- The token is stored only on the device, never in the repo.
- If two devices change data at the same time, the most recent save wins.
- Live rate works in the installed app; offline it uses the last saved rate.
