# beedlethepoet.com

Static HTML site for [beedlethepoet.com](https://beedlethepoet.com), built for GitHub Pages.

## Files

```
index.html          — home page
about.html          — about Beedle / Bre Legan
poems.html          — selected poems
zines.html          — zine catalog
events.html         — event booking info + FAQ
commissions.html    — commission a poem
contact.html        — contact form
css/style.css       — all styles
```

## GitHub Pages Setup

1. Create a new GitHub repository (e.g. `beedlethepoet`)
2. Upload all these files to the repo (keeping folder structure)
3. Go to **Settings → Pages**
4. Under **Source**, select `Deploy from a branch` → `main` → `/ (root)`
5. Save — your site will be live at `https://yourusername.github.io/beedlethepoet/`

## Custom Domain (beedlethepoet.com)

1. In your GitHub Pages settings, enter `beedlethepoet.com` as the custom domain
2. Create a file called `CNAME` in the root of your repo containing just: `beedlethepoet.com`
3. In your domain registrar's DNS settings, add these records:
   - A record: `@` → `185.199.108.153`
   - A record: `@` → `185.199.109.153`
   - A record: `@` → `185.199.110.153`
   - A record: `@` → `185.199.111.153`
   - CNAME: `www` → `yourusername.github.io`

DNS changes can take up to 24–48 hours to propagate.

## Contact Form

The contact form uses [Formspree](https://formspree.io) (free tier works great).

1. Sign up at formspree.io
2. Create a new form
3. Copy your form ID (looks like `xabcdefg`)
4. In `contact.html`, replace `YOUR_FORM_ID` with your actual ID:
   `action="https://formspree.io/f/YOUR_FORM_ID"`

## Adding Poems

To add a poem to `poems.html`, copy this block and paste it before the closing `</section>`:

```html
<div class="poem-card">
  <p class="poem-title">poem title &nbsp;·&nbsp; year</p>
  <div class="poem-body">your poem text here
line breaks work naturally
just type them in</div>
</div>
```

## Fonts

The site uses Google Fonts:
- **Special Elite** — the main typewriter-style font
- **Courier Prime** — fallback monospace
- **Playfair Display** — italic serif for subtitles and pull quotes

These load from Google Fonts CDN, so no files needed.
