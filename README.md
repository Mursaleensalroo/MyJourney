# Career Quest — an 8-bit chess journey

A self-contained, auto-looping pixel-art animation of a career told as a knight's
tour across a chessboard. Pure static site: one `index.html`, no build step.

## Deploy to Vercel

Pick whichever is easiest:

### A. Vercel CLI (fastest)
```bash
npm i -g vercel      # once
cd career-quest
vercel               # follow prompts -> preview URL
vercel --prod        # promote to production
```

### B. GitHub -> Vercel (auto-deploys on push)
```bash
cd career-quest
git remote add origin https://github.com/<you>/career-quest.git
git branch -M main
git push -u origin main
```
Then go to vercel.com -> Add New -> Project -> Import the repo -> Deploy.
Framework preset: **Other** (it's static; no settings needed).

### C. Drag & drop
Go to vercel.com/new and drop this folder in.

## Local preview
Just open `index.html` in a browser, or:
```bash
npx serve .
```

## Customising
- Captions / years / order live in the `CAP` and `M` arrays near the top of the
  `<script>` in `index.html`.
- Colours are in the `acc` palette array.
- Only external dependency is the Google "Press Start 2P" font (loaded via
  `<link>`). Ask and it can be embedded for a zero-dependency, offline build.
