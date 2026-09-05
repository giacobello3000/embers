# Embers — Streak Tracker (Web App)

A no-Xcode, no-Mac version of the streak tracker. Runs entirely in Safari, works offline once loaded, and can live on your home screen like a real app.

## Fastest way to try it
Just open `index.html` on your iPhone (AirDrop it to yourself, or email/upload it somewhere you can tap it from). Safari will open it right away — no server needed.

## Add it to your Home Screen (recommended)
1. Open the app in **Safari** on your iPhone (not Chrome — "Add to Home Screen" needs Safari for full-screen mode).
2. Tap the **Share** icon (square with an arrow).
3. Tap **Add to Home Screen**.
4. Give it a name (e.g. "Embers") and tap **Add**.

It'll now appear as its own icon and open full-screen, without Safari's address bar — it feels like a real app.

## Hosting it properly (optional, gives it a real URL)
Opening the file directly works fine, but hosting it gives you a shareable link and makes "Add to Home Screen" behave a bit more reliably:

- **Netlify Drop** — go to [app.netlify.com/drop](https://app.netlify.com/drop) and drag the `StreakWebApp` folder in. You'll get a live URL in seconds, free, no account required for a quick drop.
- **GitHub Pages** — push this folder to a GitHub repo, then enable Pages in the repo settings. Free, and stays online long-term.

Once hosted, open that URL in Safari on your iPhone and follow the Add to Home Screen steps above.

## How your data is stored
Everything (your goals and check-in history) is saved in the browser's local storage, on your device only — nothing is sent anywhere. That means:
- It stays put between visits, even offline.
- If you clear Safari's website data/history, it will be erased.
- It won't sync between devices (e.g. iPhone and iPad) since each browser stores its own copy.

## Notes on the streak logic
- Your streak doesn't reset the moment midnight hits — it only breaks once you've actually missed a full day. So if you haven't checked in yet today, it still shows yesterday's streak instead of dropping to 0.
- "Longest streak" tracks your best-ever run and doesn't get erased if your current streak later resets.
