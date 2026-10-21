# Host HTP Analytics 3D for free

## Option A: Netlify Drop (about 1 minute, no setup)
1. Go to https://app.netlify.com/drop and sign up for free.
2. Drag the whole `3d` folder (with `index.html` and `assets/`) onto the page.
3. Netlify gives you a link such as `https://htp-analytics-3d.netlify.app`. In Site settings you can rename it.
4. To update later, open the site → Deploys, then drag the folder again.

## Option B: GitHub Pages
1. Create a free GitHub account, then a new repository named `htp-analytics-3d`.
2. Upload `index.html` and the `assets/` folder.
3. Go to Settings → Pages, set Source to "Deploy from a branch", choose Branch: `main` / root, and save.
4. The link is `https://YOUR-USERNAME.github.io/htp-analytics-3d/`.

## Option C: Cloudflare Pages
Go to https://pages.cloudflare.com, then Create project → Direct upload, and upload the folder.

## Then in Tableau
1. Ask your Tableau admin to allow web page objects and add your new domain (for example `*.netlify.app`) to the safe list. In Tableau Cloud this is Settings → Web Page Objects.
2. Open `HTP Analytics 3D.twb`, double-click the Web Page object, and paste your new link in place of `https://YOUR-HOST/...`.
3. Publish.

## Important
- Free hosts are public: anyone with the link can open the page. The page holds dashboard names and links. The dashboards themselves still need a Tableau login. Check with your security team before you publish.
- **Logo:** put the official Vodafone logo file (from your brand team) in `assets/`, then set `logo: "assets/your-file.png"` in the EDIT HERE block at the top of `index.html`.
