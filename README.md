# Aurora Music

A free, ad-free, installable music player (PWA) for desktop, Android and iOS.

## Features
- Play audio files selected from your device (browser-supported formats such as MP3, WAV, M4A, AAC, OGG, FLAC).
- Local library stored in IndexedDB in that browser on that device.
- Search Internet Archive's audio collections and stream an available audio file.
- Favorites, playlists, shuffle, repeat, seek and volume.
- Responsive premium dark interface.
- No ad SDK, analytics, subscription, backend, or account required.

## Important limits
- This is a PWA, not a native App Store / Play Store app.
- Local uploads stay in the browser on the device where you added them. They are not uploaded to a cloud server and do not automatically sync between devices.
- Browser storage can be cleared by the user or reclaimed by the browser. Keep your original audio files backed up.
- Online discovery uses Internet Archive's public metadata/search endpoints. Some items may not play, may be removed, or may have restrictions. Open the item's details page and verify its rights/license before reuse. Do not assume all Internet Archive audio is public domain.
- Background playback and installation behavior vary by browser and operating system. iOS may pause audio under some system conditions.
- Free static hosting is suitable for the app code, but it does not provide free unlimited cloud storage or bandwidth for user-uploaded songs.

## Run locally
1. Unzip the project.
2. Open a terminal in the project folder.
3. Run a local static server, for example:
   - Python: `python -m http.server 8000`
   - Node: `npx serve .`
4. Visit `http://localhost:8000`.

Opening `index.html` directly may prevent service-worker installation; use localhost or HTTPS.

## Free deployment with GitHub Pages
1. Create a free GitHub account at https://github.com.
2. Create a new public repository, for example `aurora-music`.
3. Upload all project files and folders from this package to the repository root.
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Choose branch **main** and folder **/(root)**, then save.
7. Wait for GitHub Pages to publish. Your site URL will look like `https://YOUR-USERNAME.github.io/aurora-music/`.
8. Open that HTTPS URL on your devices.

## Install
- Android / desktop Chromium: open the deployed URL, then use the browser's Install app / Add to Home screen option.
- iPhone / iPad: open the URL in Safari → Share → Add to Home Screen.
- Computer: use the install icon in the browser address bar when available.

## Add music
Tap **Add your music** or the plus button and select audio files. The files are stored locally in that browser's IndexedDB. They are not sent to GitHub Pages or any other server.

## Online music
Use **Explore online** and search for a term such as `ambient`, `jazz`, `classical`, or `folk`. The app searches Internet Archive audio collections. Select Play to stream a playable audio file. Select Info to inspect the item's source page and license information.

## Privacy
The app contains no advertising code or analytics. The browser makes requests to Google Fonts (for typography) and Internet Archive (for online search/metadata/audio). You can remove the Google Fonts import in `styles.css` to avoid that third-party font request; the page will use fallback fonts.
