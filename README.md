# Drive With Kelly

A simple static website for Kelly's automatic driving lessons, hosted on GitHub Pages at [drivewithkelly.co.uk](https://drivewithkelly.co.uk).

## Local preview

Open `index.html` in a browser, or run a local server:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000

## GitHub Pages setup

1. Push this repository to GitHub (`drivewithkelly/drivewithkelly.github.io`).
2. Go to **Settings → Pages**.
3. Set **Source** to **Deploy from a branch**, branch **main**, folder **/ (root)**.
4. Under **Custom domain**, enter `drivewithkelly.co.uk` and save.
5. Once DNS has propagated, enable **Enforce HTTPS**.

The `CNAME` file in this repo already contains `drivewithkelly.co.uk`.

## DNS configuration

At your domain registrar, add:

**For the apex domain (`drivewithkelly.co.uk`):**

| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

**For www (optional):**

| Type | Name | Value |
|------|------|-------|
| CNAME | www | drivewithkelly.github.io |

DNS changes can take up to 24 hours to propagate.

## Adding a photo

1. Save a portrait photo as `assets/kelly.jpg`.
2. In `index.html`, uncomment the `<img>` line in the About section.

## Structure

```
index.html       — main page
css/styles.css   — styles
favicon.svg      — site icon
CNAME            — custom domain
assets/          — optional images
```
