# Screen Recorder + Landing Page

One repo, two pages, built for **Mfon the Digital Skills Trainer**.

- `index.html` — the landing page people land on first (email-gated download)
- `recorder.html` — the actual Screen Recorder app

## Before you publish — 1 thing to replace

Open `index.html` and find this line near the bottom:
```
const FORM_ENDPOINT = "https://formspree.io/f/REPLACE_WITH_YOUR_FORM_ID";
```
Sign up free at [formspree.io](https://formspree.io), create a new form, and replace `REPLACE_WITH_YOUR_FORM_ID` with the ID it gives you.

The download link is already wired to `recorder.html` in this same repo — nothing else to change there.

## How to publish it

1. Create a new, empty repository on GitHub (e.g. `screen-recorder`)
2. From inside this folder:
   ```
   git init
   git add .
   git commit -m "Initial commit: landing page + screen recorder"
   git branch -M main
   git remote add origin https://github.com/yourusername/screen-recorder.git
   git push -u origin main
   ```
3. Go to Settings → Pages, select the `main` branch, and save
4. Your landing page goes live at `https://yourusername.github.io/screen-recorder/`
   The recorder itself is reachable directly at `https://yourusername.github.io/screen-recorder/recorder.html`

## How the download works

The landing page's button links to `recorder.html` with the `download` attribute, so clicking it after signup saves the file straight to the visitor's device — no separate hosting needed.

## Important: run the recorder locally

Screen-recording permission can be unreliable on some hosted pages depending on the browser and viewing context. If the hosted version at `/recorder.html` doesn't prompt for screen share properly, download the file instead (that's exactly what the landing page button does) and open it locally by double-clicking — that always works.

## Tracking signups

Every submission lands in your Formspree dashboard with name, email, and timestamp.

## License

MIT — free to use, modify, and share.
