# ARQ portfolio — how to publish and update

## What's in this folder
- `index.html` — the whole site (all images are built in).
- `config.js` — your private settings (the Web3Forms key). Set once, never replaced.
- `blog/posts.js` — your ARQ./24 articles. This is the only file you edit for a new post.
- `blog/*.png` — the posters.
- Upload the folder exactly like this; keep `blog/` next to `index.html`.

## 1. Publish for free (GitHub Pages, ~10 minutes, once)
1. Create a free account at github.com (use santhoshmuthu910@gmail.com).
2. Click "+" → New repository. Name it `arq-portfolio`. Public. Create.
3. On the empty repo page click "uploading an existing file". Drag in `index.html`,
   `README.md` and the whole `blog` folder. Click "Commit changes".
4. Repo → Settings → Pages → Build and deployment → Source: "Deploy from a branch",
   Branch: `main`, folder `/ (root)` → Save.
5. After ~1 minute your site is live at `https://<your-username>.github.io/arq-portfolio/`.
   (Settings → Pages shows the exact link.)
6. Optional, later: buy a domain (e.g. santhoshmuthu.co.uk, ~£5–10/year) and add it under
   Settings → Pages → Custom domain. GitHub gives you HTTPS for free.

Alternative, if you'd rather not touch GitHub: drag this folder onto https://app.netlify.com/drop
(free, instant link like `arq-portfolio.netlify.app`). Updates = drag the folder again.

## 2. Get enquiries delivered to your email (Web3Forms, free, ~2 minutes, once)
1. Go to https://web3forms.com → enter santhoshmuthu910@gmail.com → "Create Access Key".
2. Open the email they send you and copy the access key.
3. Open `config.js`, paste the key between the quotes, and save/upload it. That's the only place the key lives,
   so replacing `index.html` later never erases it.
Every message from the site's contact form lands in your inbox with the sender's name and email. The visitor sees
a "Thanks, your message is on its way" note on the same page (no new page). If the key is missing the form opens
the visitor's email app instead. Free plan: 250 messages a month, spam protection included.

## 3. Publish a new ARQ./24 post every day (~2 minutes)
1. Save the day's poster as `blog/ARQ24_DayXX_Name.png`.
2. Open `blog/posts.js`. Copy one `{ ... },` block, paste it at the top of the list and change:
   `day`, `date` (YYYY-MM-DD), `cat`, `region`, `read`, `accent` (orange word on the card),
   `poster` (the file name), `alt` (what the poster shows), and the article text between the backticks.
   Article format: `# Title`, then `## Section` headings, normal paragraphs, `- bullets`,
   `**bold**`, links as plain URLs. Put `[image: ...]` on its own line where the poster should appear.
3. On GitHub: open the repo → `blog` → `posts.js` → pencil icon → paste → "Commit changes".
   Then `blog` → "Add file" → "Upload files" → drop the poster → Commit. Live in about a minute.
   (On Netlify Drop: drag the whole folder again.)

Or send Claude the article link and the poster, as you do now, and Claude will add it and give you
the updated files. If you connect GitHub in claude.ai → Settings → Connectors, Claude can push it
straight to the live site for you.
