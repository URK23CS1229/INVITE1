# காயத்ரி & அபினேஷ் — Engagement Invitation

A pink-lotus, animated Tamil engagement invitation. Plain HTML + CSS + JavaScript. No frameworks, no build step.

## Folder layout

```
lotus-invite/
├── index.html                 ← page structure + all SVG lotus illustrations
├── css/style.css              ← colours, layout, animations
├── js/config.js               ← ★ EDIT THIS: names, date, time, map link, messages
├── js/main.js                 ← envelope animation, music, petals, countdown
├── assets/
│   ├── fonts/                 ← Tamil + English fonts (bundled, work offline)
│   ├── music/background-music.mp3
│   └── favicon.svg
└── .nojekyll                  ← tells GitHub Pages to serve files as-is
```

## Run it in VS Code (Windows)

1. Unzip the folder, e.g. to `C:\Users\<you>\Documents\lotus-invite`.
2. VS Code → **File → Open Folder…** → pick `lotus-invite`.
3. Extensions (Ctrl+Shift+X) → install **Live Server** (by Ritwick Dey).
4. Right-click `index.html` → **Open with Live Server**.
5. The browser opens at `http://127.0.0.1:5500/`. Every save reloads the page.

To test on your phone: phone and laptop on the same Wi-Fi, then open
`http://<laptop-IP>:5500` on the phone. Find the IP in PowerShell with `ipconfig` (IPv4 Address).

## Publish on GitHub Pages

```powershell
cd C:\Users\<you>\Documents\lotus-invite
git init
git add .
git commit -m "Engagement invitation"
git branch -M main
git remote add origin https://github.com/<your-username>/gayathri-abinesh.git
git push -u origin main
```

(Create the empty repo `gayathri-abinesh` on github.com first — Public, no README.)

Then on GitHub: repo → **Settings → Pages** → Source: **Deploy from a branch** →
Branch: **main**, folder **/ (root)** → **Save**.
After 1–2 minutes the site is live at:
`https://<your-username>.github.io/gayathri-abinesh/`

To update later: edit → `git add .` → `git commit -m "update"` → `git push`.

## Customise

| Want to change… | Edit | Example |
|---|---|---|
| Names, date, time, messages | `js/config.js` | `timeText: "காலை 10:00 மணி முதல் 11:00 மணி வரை"` |
| Venue name shown on the card | `venueName` in `js/config.js` | `venueName: "ஸ்ரீ மஹால், கோவை"` |
| Map location | `mapUrl` in `js/config.js` | paste a new Google Maps share link |
| Countdown target | `eventStartISO` | `"2026-12-04T12:00:00+05:30"` |
| Seal letters | `initial1`, `initial2` | `"G"`, `"A"` |
| Hide the "உ" at the top | `topBlessing: ""` | |
| Music | replace `assets/music/background-music.mp3` (keep the name) or change `music:` | |
| Music loudness | `musicVolume` (0 – 1) | `0.4` |
| Colours | `:root` at the top of `css/style.css` | `--lotus: #d6547f;` |
| Animation speed of the envelope | the `wait(…)` numbers in `openInvitation()` in `js/main.js` | `wait(1250)` → `wait(1600)` = card stays longer |
