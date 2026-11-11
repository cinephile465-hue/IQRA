# Engineering Guide by IQRA

The KTU civil engineering syllabus as 3D lessons that students can turn, pause and change. Made by Azam Ahammed, B.Tech Civil Engineering student.

The whole app is one file, `index.html`. It needs no server, no database and no build step. It runs in any modern browser on phones and computers.

## What is built

- **Landing page** with four looks (Cinematic, Playful, Ink, Studio), an animated truss bridge, and a scroll demo where a rough line turns into a real beam.
- **5 subjects open:** Engineering Mechanics, Mechanics of Solids, Fluid Mechanics, Structural Analysis I, and Surveying and Geomatics. That is 108 lessons with live 3D scenes, plus theory pages.
- **Syllabus map** that checks every topic against both the KTU 2019 and the KTU 2024 syllabus, and says honestly what is not covered yet.
- **Drawing studio:** draw a beam, truss, frame, notch or weir, open channel, dam wall or level book. The app solves it and shows it in 3D with every reaction and force. There are also influence lines and moving loads.
- **Teach mode** for lessons, and a **teacher's board** (full-screen pen, highlighter, arrow, eraser, undo, save as picture) on lessons and the drawing studio.
- **Gallery** of real structures in 3D.
- **Sign-in with name and Gmail** (no password). Progress is saved on the student's own device.
- **Page not found** screen, a friendly message when something fails, and an **error log** at `#/errors`.
- **Installable:** "Add to Home screen" gives an app icon named "Eng Guide".

## What is not built yet

- More subjects: their topic lists are shown, marked "Coming soon".
- "Type a question, get the figure" (shown as Coming soon on the landing page).
- Progress that follows a student to another phone. Today it stays on one device.
- "Continue with Google" sign-in.
- Error reports sent to the developer. Errors are only kept on the student's device.
- A version for mechanical engineering.

## Planned next

1. Recolour the 3D lesson scenes to match the chosen look.
2. Open the next civil subjects.
3. Optional later: online accounts (for example Firebase) so progress syncs across devices, plus Google sign-in.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app |
| `404.html` | The "Page not found" page GitHub shows for a wrong address |
| `og.png` | The picture shown when the link is shared on WhatsApp or Telegram |
| `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` | Home-screen icons |
| `manifest.webmanifest` | Name and icons for "Add to Home screen" |

## Services the app depends on

| Service | Used? | Notes |
|---|---|---|
| Hosting | GitHub Pages (free, public repository) | Upload all the files above to the root of the repository |
| Domain | Not yet (free GitHub address) | Live at `https://cinephile465-hue.github.io/IQRA/` |
| Database | None | Accounts and progress live in the browser's own storage on each device |
| Sign-in provider | None | Name and Gmail are only labels on the device |
| Payments | None | |
| Error tracking service | None | Errors are logged on the device only (`#/errors`) |
| Fonts, scripts or images from other sites | None | Everything is inside `index.html` |

**Environment variables:** none. The app has no secret keys or passwords anywhere in the code. If Google sign-in or an online database is added later, they will need public configuration values (for example `GOOGLE_CLIENT_ID` or `FIREBASE_API_KEY`). Keep anything truly secret out of this public repository.

## Updating the site

Upload the new `index.html` to the same repository and commit. GitHub Pages republishes it within a few minutes.
