# Digging Deeper — static blog

A plain HTML blog. No build step, no dependencies. Edit files, push, done.

## Files

- `index.html` — the home page + list of writings
- `posts/` — one HTML file per writing
- `posts/_TEMPLATE-post.html` — copy this to start a new post
- `og-default.png` — the image shown when a link is shared
- `404.html` — shown for bad links

The sample post (`the-god-who-hides.html`) is a placeholder to show the format. Delete it or replace it with your own.

## Put it online (new GitHub account)

- Create the new GitHub account yourself (I can't make accounts or log in for you)
- Make a new repo. Two options:
  - name it `yourusername.github.io` → site lives at `https://yourusername.github.io/`
  - name it anything, e.g. `blog` → site lives at `https://yourusername.github.io/blog/`
- Upload all these files (drag them into the repo's "Add file" → "Upload files")
- Repo → Settings → Pages → Source: `main` branch, `/root` → Save
- Give it a minute, then load the URL

## Share URLs — already done

The share tags are already set to `https://diggingdeeperdc.github.io/`, so link previews (the card + image on Facebook/WhatsApp/etc.) will work once the site is live. Nothing to change.

(If you ever move to a custom domain, find-and-replace `diggingdeeperdc.github.io` with your new domain across the files.)

## Heads up: GitHub Pages + Facebook sharing

GitHub Pages sometimes serves pages with an HTTP `206` response, which Facebook's link scraper chokes on — the preview card comes back blank or broken. Two fixes:

- Best: put **Cloudflare** (free plan) in front of the site as a proxy. Fixes it reliably and speeds the site up.
- Test/refresh a link anytime with the **Facebook Sharing Debugger** (search that name) — paste your URL, hit "Scrape Again" to force a fresh preview.

## Add a new writing

1. Copy `posts/_TEMPLATE-post.html`, rename it e.g. `posts/grace-and-effort.html`
2. Edit the title, date, and your text (first letter becomes a drop cap automatically)
3. For a scripture quote, use the `<blockquote>` block already in the template
4. Add a matching entry on `index.html` — copy the `<li class="entry">` block and point it at your new file
5. Replace `REPLACE-WITH-YOUR-URL` in the new file

## Custom domain (optional)

- Buy a domain, add a file named `CNAME` containing just your domain (e.g. `deeperwaters.com`)
- Point the domain's DNS at GitHub Pages (or at Cloudflare if using it)
- Update the URL placeholder to your domain

## Change the look

Styling lives in the `<style>` block at the top of each HTML file. Colours are the CSS variables (`--paper`, `--ink`, `--accent` etc.) — change them in one file to preview, then match the others.
