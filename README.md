# Lake Calavera Preserve Field Guide

A mobile-first native species field guide for Lake Calavera Preserve, Carlsbad CA.  
A California Naturalist Stewardship Project by Adriel Hampton, Spring 2026.  
Sponsored by [Preserve Calavera](https://www.preservecalavera.org).  
Live at **[LakeCalavera.com](https://lakecalavera.com)**

## What this is

A self-contained HTML field guide to native plants, birds, reptiles & amphibians, mammals, and insects of Lake Calavera Preserve. Photos are loaded live from iNaturalist — no backend required, no maintenance needed. Species cards link directly to iNaturalist observations filtered to the preserve's boundary.

## How to update

Edit `index.html` and push to GitHub. The site updates within a minute or two automatically.

**To update or add one of Adriel's observation photos:**
1. Find the `OBS_IDS` object in the `<script>` section
2. Add or update: `'Scientific name': observationId,`  
   (The observation ID is the number at the end of the iNaturalist URL)
3. Save and push

**To add a new species card:**
1. Find the `SPECIES` array
2. Add a new entry following the existing format:
```javascript
{common:'Common Name', sci:'Scientific name', hab:'css', note:'Field note for visitors.'},
```
- `hab` values: `'css'` (Coastal Sage Scrub), `'chap'` (Chaparral), `'rip'` (Riparian), `'wild'` (Wildflowers), `'bird'`, `'herp'`, `'mammal'`, `'insect'`
- For species appearing in multiple tabs, use an array: `hab:['css','chap']`
- Optional: `status:'rare'`, `status:'sensitive'`, `status:'venomous'`, or `status:'caution'`
3. Save and push

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `calavera-guide`)
2. Upload `index.html`
3. Go to **Settings → Pages**
4. Under **Source**, select `Deploy from a branch`
5. Select branch: `main`, folder: `/ (root)`
6. Click Save
7. Your guide will be live at: `https://[yourusername].github.io/calavera-guide`

## Custom domain (LakeCalavera.com)

The guide is served at [LakeCalavera.com](https://lakecalavera.com) via a custom domain on GitHub Pages.  
DNS is managed through Namecheap pointing to GitHub's servers.

## Embedding on external websites

Add this iframe to any WordPress page:

```html
<iframe 
  src="https://lakecalavera.com" 
  width="100%" 
  height="800px" 
  frameborder="0"
  style="border:none; border-radius:12px;">
</iframe>
```

Adjust height as needed. The guide is fully responsive and works on all screen sizes.

## Contact & feedback

Questions or feedback: [lakecalavera@adrielhampton.com](mailto:lakecalavera@adrielhampton.com)

## Credits

- Native plant list: James Dillane, 2017 survey of Lake Calavera & Calavera Heights Preserves
- Photos: Adriel Hampton and iNaturalist community contributors (Creative Commons license)
- Developed as a UC California Naturalist Certification Stewardship Project
