# Static Slides Launcher (static site)

This is a small static site that:
- Shows a launcher grid of presentations (tiles).
- Lets a user paste a Google Slides ID or full Slides URL and open it in a viewer that embeds the official Google Slides embed.

Files
- index.html — launcher and manual entry
- viewer.html — embeds Slides by ID using Google's embed URL
- styles.css — site styling

How to use / deploy
1) Put these files into a single folder (e.g., SlidesLauncher).
2) Deploy to Netlify (recommended, fast):
   - Go to https://app.netlify.com/drop
   - Drag & drop the folder (or zip) onto the page.
   - Netlify will upload and host it; you'll get a public URL you can share.

3) Or use GitHub Pages:
   - Create a GitHub repo, push these files to the repository root, then enable Pages in repository Settings → Pages (select main branch, root).
   - Site will be available at https://<yourusername>.github.io/<repo>

4) Testing locally (optional):
   - You can open index.html directly in a browser for basic testing.
   - For viewer.html query parameters to work consistently, run a simple static server:
     - Install a static server if you have Node: `npm install -g http-server`
     - Run `http-server` in the folder and open the provided localhost URL.

Tips
- Replace or extend the `tiles` array in index.html to add more tiles.
- For each tile URL you can use:
  - viewer.html?id=<ID>
  - https://docs.google.com/presentation/d/<ID>/embed
  - Or any public URL you want users to open.
- Remember: the embedded Slides must be shared as "Anyone with the link" or published for others to view.

If you want, I can:
- Pre-fill the tiles array with more of your presentation IDs.
- Generate a QR code image URL you can insert into a slide that links to your hosted launcher.
- Walk you step-by-step to drag & drop these files to Netlify and get the public URL.