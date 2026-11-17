# Super Zoom Pro Camera — Vercel PWA for iPhone 13 Pro Max

This is a browser-based installable camera app. You do **not** need a Mac, Xcode, or App Store publishing to use it.

## Deploy using only your iPhone
1. Download and unzip this project.
2. Open https://vercel.com in Safari and sign in (or create an account).
3. The simplest deployment path is to create a GitHub repository and upload these files, then import that repository in Vercel. Alternatively use Vercel's supported deployment workflow from a computer if available.
4. In Vercel choose **Add New → Project**, import the repository, and deploy. No build command is required; output is the project root.
5. Open the deployed `https://...vercel.app` URL in Safari on your iPhone.
6. Tap **Start Camera** if prompted (browser will ask permission). Then use Share → Add to Home Screen.

## Features
- Responsive professional camera interface for iPhone Safari
- Rear/front camera switching
- 1×–200× digital zoom slider and presets
- Tap-to-focus marker (actual focus support depends on browser/device APIs)
- Photo capture and session gallery with download/save actions
- Video recording when MediaRecorder is supported
- Moon and Night guidance presets
- Installable PWA shell and basic offline caching

## Honest hardware/browser limitations
- The iPhone 13 Pro Max has 3× optical telephoto zoom. A web app cannot promise true 200× optical zoom; values above the physical lens range are digital enlargement and quality falls sharply.
- iOS Safari may expose the rear camera as one logical device rather than offering reliable direct selection among all three lenses. Lens selection and hardware zoom are controlled by iOS/browser.
- Camera use requires HTTPS and permission. iOS may stop the camera when Safari is backgrounded, the phone is locked, or the app is suspended. A web app cannot guarantee background camera operation.
- Photos/videos are downloaded to the iPhone from the browser; this starter does not silently write to the Photos library.
- This is a PWA, not a signed native iOS application.

## Files
- `index.html` — camera UI and capture logic
- `public/manifest.webmanifest` — installable web app metadata
- `public/sw.js` — basic offline shell cache
- `public/icon.svg` — app icon
- `vercel.json` — Vercel headers
