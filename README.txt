# Team Kudos — Setup Instructions

## Files in this package
- `index.html` — the kudos app (host this)
- `config.html` — Teams tab configuration page (host this)
- `manifest.json` — Teams app manifest
- `color.png` — app icon 192x192 (ADD THIS: create a 192x192 PNG icon)
- `outline.png` — app icon 32x32 white outline (ADD THIS: create a 32x32 white PNG icon)

---

## Step 1 — Host the app (free option: GitHub Pages)

1. Create a free GitHub account at github.com
2. Create a new repository, e.g. `team-kudos`
3. Upload `index.html` and `config.html` to the repository
4. Go to Settings → Pages → Source: main branch → Save
5. Your URL will be: `https://YOUR-USERNAME.github.io/team-kudos`

---

## Step 2 — Update the URLs

Replace `YOUR-HOSTED-URL` in these files with your actual URL:

**manifest.json** — update:
- `developer.websiteUrl`
- `configurableTabs[0].configurationUrl`
- `staticTabs[0].contentUrl` and `websiteUrl`
- `validDomains[0]`

Also replace `YOUR-UNIQUE-GUID-HERE` in the `id` field with a real GUID.
Generate one free at: https://www.guidgenerator.com

**config.html** — update the two `YOUR-HOSTED-URL` references in the setConfig() call.

---

## Step 3 — Add icons

Teams requires two icon files in the zip:
- `color.png` — 192×192 pixels, full color
- `outline.png` — 32×32 pixels, white/transparent

You can create simple ones at canva.com or use any image editor.

---

## Step 4 — Package the app

Zip these 4 files together (NOT the folder, the files directly):
- manifest.json
- index.html
- config.html
- color.png
- outline.png

Name it: `team-kudos.zip`

---

## Step 5 — Upload to Microsoft Teams

1. Open Microsoft Teams
2. Click **Apps** in the left sidebar
3. Click **Manage your apps** → **Upload an app** → **Upload a custom app**
4. Select your `team-kudos.zip`
5. Click **Add to a team**, select your channel, click **Set up a tab**

> Note: Your Teams admin must have "Upload custom apps" enabled.
> They can enable it at: Teams Admin Center → Teams apps → Setup policies

---

## Step 6 — Add to a channel

Once uploaded:
1. Go to your team channel
2. Click **+** next to the tab bar
3. Find **Team Kudos** and click it
4. Click **Save**

The Kudos tab is now live for your whole team! 🎉
