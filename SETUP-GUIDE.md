# Retirement Cockpit — iPhone Home-Screen App Setup

This folder is everything needed to run the Cockpit as an app on your iPhone:
its own icon, full-screen with no browser bars, works offline, autosaves on the phone.

**Privacy first:** `index.html` here contains **no financial data** — all values are
zero/neutral. Your real figures go onto your phone in step 3 and live **only on your
phone**, never on the hosting service.

---

## Step 1 — Host the folder (one-off, ~5 minutes)

### Option A: GitHub Pages (free, recommended)
1. Create a free account at github.com if you don't have one.
2. Click **+ → New repository**. Name it e.g. `cockpit`. Set it to **Private? No — choose Public**
   (Pages on free accounts needs a public repo; this is fine because the app contains no data).
3. On the new repo page: **uploading an existing file** → drag in ALL files from this
   folder (`index.html`, `manifest.json`, `sw.js`, the three `icon-*.png`) → **Commit changes**.
4. Go to **Settings → Pages** → under "Branch" choose `main` and `/ (root)` → **Save**.
5. After a minute, the page shows your address, e.g.
   `https://YOURNAME.github.io/cockpit/` — that's your app's home.

### Option B: Netlify Drop
1. Go to `app.netlify.com/drop` (free account needed).
2. Drag this whole folder onto the page. It gives you an address like
   `https://something.netlify.app` immediately.

> Tip: the address is unguessable in practice, but it is public — which is exactly why
> this copy ships with blank data.

## Step 2 — Install on your iPhone
1. Open the address from Step 1 in **Safari** on the phone (must be Safari).
2. Tap the **Share** button (square with arrow) → **Add to Home Screen** → **Add**.
3. A "Cockpit" icon (gold gauge on green) appears on your home screen.
   Opening it gives the full-screen app. After the first visit it also works offline.

## Step 3 — Get your data onto the phone (once)
1. On the computer where you've been using your personal Cockpit file:
   open it → **Reports → Save scenario (JSON)**. Send that file to your phone
   privately (AirDrop is ideal; it never touches the internet).
2. On the phone, open the Cockpit app → **Reports → Load scenario (JSON)** →
   pick the file. Everything appears, and from then on autosaves on the phone.
3. Delete the JSON from the phone's Files app if you like — the app has its own copy.

## Keeping things in sync
- Phone and computer each keep their **own** autosaved copy. To move changes between
  them, use **Save scenario (JSON)** on one and **Load scenario (JSON)** on the other
  (or "Download app + data" for an all-in-one file — keep that file private).

## Updating the app later
- If you receive an updated `index.html`, upload it to the same repo replacing the old
  one (and bump nothing else). On the phone, open the app online once; pull-to-refresh
  if needed. Your data is untouched — it lives in the phone's storage, not the file.

## Troubleshooting
- **"Add to Home Screen" missing** → you're in Chrome or a Google app's browser; use Safari.
- **Old version showing** → the offline cache is serving the previous copy. Visit the
  address in Safari (not the icon) once while online, refresh, then reopen the icon.
- **Data gone after clearing Safari data** → "Clear History and Website Data" wipes
  home-screen app storage too. Restore from your latest JSON export — which is why an
  occasional **Save scenario (JSON)** backup is a good habit.

---
*This is a planning tool, not financial advice. UK figures based on 2025/26 allowances.*
