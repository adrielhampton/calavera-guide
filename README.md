# Lake Calavera Preserve Field Guide

A mobile-first native species field guide for Lake Calavera Preserve, Carlsbad CA.  
A California Naturalist Stewardship Project by Adriel Hampton, Spring 2026.  
Sponsored by [Preserve Calavera](https://www.preservecalavera.org).

## What this is

A self-contained HTML field guide to native plants, birds, reptiles & amphibians, mammals, and insects of Lake Calavera Preserve. Photos are loaded live from iNaturalist — no backend required, no maintenance needed.

## How to update

Edit `index.html` and push to GitHub. The site updates within a minute or two automatically.

To add a new species observation photo:
1. Find the `OBS_IDS` object in the `<script>` section
2. Add: `'Scientific name': observationId,`
3. Save and push

To add a new species card entirely:
1. Find the `SPECIES` array
2. Add a new entry following the existing format
3. Save and push

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `calavera-guide`)
2. Upload `index.html` and rename it to `index.html` (it already has this name)
3. Go to **Settings → Pages**
4. Under **Source**, select `Deploy from a branch`
5. Select branch: `main`, folder: `/ (root)`
6. Click Save
7. Your guide will be live at: `https://[yourusername].github.io/calavera-guide`

## Embedding on the Preserve Calavera website (for Paige)

Add this iframe to any WordPress page:

```html
<iframe 
  src="https://[yourusername].github.io/calavera-guide" 
  width="100%" 
  height="800px" 
  frameborder="0"
  style="border:none; border-radius:12px;">
</iframe>
```

Adjust height as needed. The guide is fully responsive and works on all screen sizes.

## Credits

- Native plant list: James Dillane, 2017 survey of Lake Calavera & Calavera Heights Preserves
- Photos: Adriel Hampton and iNaturalist community contributors (Creative Commons license)
- Developed as a UC California Naturalist Certification Stewardship Project
