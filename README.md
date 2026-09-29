# Kyle Utley — Portfolio Site (self-hosted export)

This is your portfolio site as plain files — no dependency on claude.ai at all.
Everything (images, resumes) is included locally in this folder.

## What's inside
- `index.html` — the site
- `assets/` — all project photos and CAD renders
- `resumes/` — Core, Manufacturing, and Defense/Aero resume PDFs

## Fastest way to get this live on your own domain (free hosting)

### 1. Buy a domain
Any registrar works — Namecheap, Cloudflare, Google Domains successor, etc.
Something like `kyleutley.com` or `kylejutley.com`. ~$10-15/year.

### 2. Put this site on GitHub Pages (free)
1. Create a free GitHub account if you don't have one.
2. Create a new repository — name it anything, e.g. `portfolio`.
3. Upload everything in this folder (`index.html`, `assets/`, `resumes/`) to
   the repository's root (drag-and-drop works fine on github.com, or use
   `git add . && git commit -m "portfolio" && git push` if you're comfortable
   with git).
4. In the repo, go to **Settings → Pages**. Under "Build and deployment,"
   set Source to "Deploy from a branch," branch `main`, folder `/ (root)`.
   Save. GitHub will give you a URL like `https://yourusername.github.io/portfolio/`
   — confirm the site loads there first.

### 3. Point your custom domain at it
1. Still in **Settings → Pages**, enter your custom domain (e.g.
   `kyleutley.com`) in the "Custom domain" field and save. GitHub will
   create a `CNAME` file in your repo automatically.
2. Go to your domain registrar's DNS settings and add these records
   (exact steps vary by registrar, but the records are standard):
   - Four `A` records for the root domain (`@`) pointing to GitHub Pages' IPs:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - A `CNAME` record for `www` pointing to `yourusername.github.io`
3. DNS changes can take anywhere from a few minutes to a few hours to
   propagate. Once it does, `kyleutley.com` will load your site directly.
4. Back in GitHub Pages settings, check "Enforce HTTPS" once it's available
   (it appears after DNS propagates) so the site loads securely.

## Resume variant links
The "Download Resume" button defaults to your Core resume. To route from a
specific resume variant instead, use:
- Manufacturing resume → `https://yourdomain.com/?resume=manufacturing`
- Defense/Aero resume → `https://yourdomain.com/?resume=defense`
- Everywhere else (LinkedIn, Core resume, business card) → the bare URL

## Updating the site later
If you want changes made again through Claude, just re-upload the new
`index.html` (and any new/changed files in `assets/` or `resumes/`) to the
same GitHub repo, overwriting the old ones. GitHub Pages updates
automatically within a minute or two of a push.
