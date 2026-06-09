# NOMU Daily Fortune

## Run in VS Code

1. Open this folder in VS Code.
2. Install the recommended **Live Server** extension when VS Code suggests it.
3. Right-click `index.html` and choose **Open with Live Server**.
4. Open `http://127.0.0.1:5500/index.html` if the browser does not open automatically.
5. Allow camera permission, then press `เปิดกล้อง`.

The app is built as a single HTML file with local assets. Live Server is recommended because webcam access works more reliably from a local server than from a direct `file://` page.

## Admin settings

Open the app and press **Admin** to edit card messages, rewards, and upload custom front/back card designs for the current browser. The demo admin code is:

```text
nomu
```

This is a GitHub Pages/static demo, so admin settings are stored in localStorage on the current device. For a real campaign across multiple devices, connect this screen to a backend or database.

## Put on GitHub Pages for mobile testing

Mobile browsers usually require HTTPS for webcam access. GitHub Pages gives you an HTTPS URL that works well for testing on a phone.

```powershell
git init
git add index.html README.md .nojekyll assets/nomu-card-back.jpg assets/nomu-card-front.jpg .vscode/settings.json .vscode/extensions.json
git commit -m "Add NOMU Daily Fortune web app"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

Then enable GitHub Pages:

1. Open the repository on GitHub.
2. Go to **Settings** > **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select branch `main` and folder `/root`.
5. Open the Pages URL from your phone and allow camera permission.

If the camera does not start on mobile, open the GitHub Pages URL directly in Chrome or Safari, not inside a social media in-app browser.
