# Life Dashboard — setup on GitHub Pages

Six files live in this folder. They are the whole app.

| File | What it is |
|---|---|
| `index.html` | The app itself |
| `sw.js` | Service worker — makes it launch offline |
| `manifest.webmanifest` | Tells iOS it's an installable app |
| `apple-touch-icon.png` | Home Screen icon |
| `icon-192.png`, `icon-512.png` | App icons |

`SETUP.md` (this file) is just notes — uploading it is optional.

---

## Before you start: save your current data

On your phone, open the **old** app (the claude.ai link), tap the **gear icon**,
tap **Export backup**, and save the file. You'll import it at step 8.

---

## 1. Create the repository

On github.com, click **+** (top right) → **New repository**.

- **Repository name:** `life-dashboard`
- **Visibility:** **Public** — GitHub Pages is only free for public repos.
  Your *code* is public; your *data* is not. Logs and photos live on your
  phone and are never uploaded here.
- Leave every checkbox unchecked (no README, no .gitignore).
- Click **Create repository**.

## 2. Upload the files

On the empty repo page, click **uploading an existing file**.

Drag in the **six files** from this folder — the files themselves, not the
folder. (Open the folder, select all, drag.)

Click **Commit changes**.

## 3. Turn on Pages

**Settings** (top of the repo) → **Pages** (left sidebar).

- **Source:** Deploy from a branch
- **Branch:** `main`, folder `/ (root)`
- **Save**

## 4. Wait, then grab the URL

Wait about a minute, refresh the Pages settings page. It will show:

```
https://YOUR-USERNAME.github.io/life-dashboard/
```

That's your app's permanent address.

## 5. Install it on your iPhone

Open that URL in **Safari** (not Chrome — only Safari can install to the
Home Screen on iOS).

Tap **Share** → **Add to Home Screen** → **Add**.

## 6. Launch from the icon

Open the app from the new Home Screen icon. It should fill the screen with no
Safari address bar — that's how you know it installed as an app.

## 7. Check storage health

Tap the **gear icon** → scroll to **Storage health**. You want:

- Installed to Home Screen: ✓
- Persistent storage: Granted
- Offline ready: ✓

## 8. Bring your data over

Still in Settings → **Import backup** → **Choose backup file** → pick the JSON
you exported at the start. Everything comes back.

## 9. Clean up

Delete the old Home Screen icon that pointed at claude.ai, so you don't log
into the wrong copy by mistake.

---

## Updating later

When Claude gives you a new `index.html`:

1. Go to your repo on github.com
2. Click `index.html` → the **pencil** icon → select all → paste the new version → **Commit changes**

Or use **Add file → Upload files** and drop the new one in to overwrite.

Your Home Screen icon and all your data stay exactly as they are — only the app
code changes. Changes appear next time you open the app.

## Troubleshooting

**404 page.** Pages takes a minute or two on first deploy. Also confirm
`index.html` sits at the top level of the repo, not inside a folder.

**Still says "Not granted" for persistent storage.** Use the app a few times and
recheck; iOS grants it once it sees the app is real. Keep exporting backups
either way.

**Data missing.** Check you opened the Home Screen icon and not a Safari tab —
they keep separate copies.
