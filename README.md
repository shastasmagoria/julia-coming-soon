# Julia coming-soon page

This folder contains a complete static website for `julia.build`.

## Files

- `index.html` contains the visible words and page structure.
- `styles.css` controls the fonts, spacing, colors, and layout.
- `CNAME` tells GitHub Pages that the site uses `julia.build`.

## Recommended free hosting: GitHub Pages

Create a new **public** GitHub repository named `julia-coming-soon`. Do not put this page in the main Julia application repository. Keeping the tiny public marketing page separate avoids exposing or tangling it with product work.

Upload all three files to the top level of that repository.

Then open:

1. Repository **Settings**
2. **Pages**
3. Under **Build and deployment**, choose **Deploy from a branch**
4. Choose branch **main** and folder **/(root)**
5. Save

Under **Custom domain**, enter:

`julia.build`

Wait until GitHub reports that its DNS check is ready before changing DNS at GoDaddy.

## GoDaddy DNS records for julia.build

In GoDaddy, open the domain, then **DNS**. Remove any conflicting website-builder connection or existing `@` A record before adding these records.

Add four A records:

| Type | Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

Add this CNAME record:

| Type | Name | Value |
|---|---|---|
| CNAME | www | shastasmagoria.github.io |

Return to GitHub Pages after the DNS check succeeds and turn on **Enforce HTTPS**.

DNS changes can take time to spread. A delay does not necessarily mean the setup failed.

## Editing the page later

For wording changes, edit `index.html`.

For visual changes, edit `styles.css`.

GitHub Pages republishes the site after each committed change.

## Second domain

After `julia.build` is working, set `juliaconstruction.com` in GoDaddy to a permanent 301 forward to:

`https://julia.build`

Use forwarding only, not masking.
