# Molly Turnbull — Cosmetologist Portfolio

Personal portfolio website for Molly Turnbull, a newly licensed cosmetologist based in Portland, Maine. Three static HTML pages, one shared stylesheet, no frameworks, no build tools, no JavaScript.

---

## Structure

```
molly-turnbull/
├── index.html        Landing page
├── portfolio.html    Photo gallery and skills
├── resume.html       Printable résumé
├── css/
│   └── style.css     All styles, responsive and print included
└── images/           Drop photo files here
```

---

## Pages

**Home (index.html)**
Introduces Molly with a portrait, a stats strip, an about section, an eco philosophy strip, and a contact section with links to email, phone, and Instagram.

**Portfolio (portfolio.html)**
A 12-slot mosaic gallery showing her work, followed by a grid of nine technique cards covering the skills she trained in.

**Résumé (resume.html)**
A print-ready résumé covering her objective, education, experience, technical skills, certifications, and references. Includes a Print / Save PDF button.

---

## Adding Photos

### Portrait (index.html)

Find this block in `index.html`:

```html
<!-- Replace with: <img src="images/portrait.jpg" alt="Molly Turnbull"> -->
<div class="portrait-placeholder">
  <div class="placeholder-icon">+</div>
  <div class="placeholder-label">Your portrait here</div>
  <div class="placeholder-sub">Replace in HTML</div>
</div>
```

Replace the entire thing with:

```html
<img src="images/portrait.jpg" alt="Molly Turnbull" />
```

### Gallery photos (portfolio.html)

Each slot looks like this:

```html
<figure class="gi">
  <!-- <img src="images/work-01.jpg" alt="Balayage color"> -->
  <div class="gi-placeholder">
    <div class="gi-num">01</div>
    <div class="gi-lbl">Balayage / Color</div>
  </div>
  <figcaption>Balayage / Color</figcaption>
</figure>
```

To add a photo, uncomment the `<img>` tag and delete the `<div class="gi-placeholder">` block:

```html
<figure class="gi">
  <img src="images/work-01.jpg" alt="Balayage color" />
  <figcaption>Balayage / Color</figcaption>
</figure>
```

Repeat for each slot. Image files go in the `images/` folder.

### Recommended image sizes

| Slot       | Spans       | Suggested size |
| ---------- | ----------- | -------------- |
| 01, 03     | 2 rows tall | 900 x 700px    |
| 06, 10     | 2 rows tall | 700 x 700px    |
| All others | 1 row       | 600 x 400px    |

JPG works well for photos. Keep files under 500KB for fast loading.

---

## Updating Personal Details

Search and replace the following placeholder values across the HTML files:

| Placeholder                | Replace with                         |
| -------------------------- | ------------------------------------ |
| `molly.turnbull@email.com` | Molly's real email address           |
| `(207) 555-0000`           | Molly's real phone number            |
| `Your Cosmetology School`  | The name of her school               |
| `20__ – 20__`              | Date range for prior work experience |
| `Company Name · Location`  | Prior employer name and location     |
| `Previous Work Experience` | Real job title                       |

The Instagram handle `@miss.molly.creations` and its URL are already correct throughout.

---

## Résumé Tips

The résumé page is print-ready. The print stylesheet hides the nav and top bar, switches to a white background, and adjusts colors for ink. To export a PDF:

1. Open `resume.html` in a browser
2. Press `Ctrl+P` (Windows) or `Cmd+P` (Mac), or click the Print button on the page
3. Choose **Save as PDF** as the destination
4. Set margins to **Default** or **Minimum**

---

## Deployment

This is a plain static site. No server, no build step required.

**GitHub Pages**

1. Push the folder to a GitHub repository
2. Go to Settings > Pages
3. Set the source to the main branch, root folder
4. The site will be live at `https://yourusername.github.io/molly-turnbull`

**Netlify**

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the `molly-turnbull` folder onto the page
3. Done — Netlify provides a shareable URL instantly

**Vercel**

1. Install the Vercel CLI or connect your GitHub repo at vercel.com
2. Run `vercel` in the project folder
3. Follow the prompts

---

## Accessibility

Gold text uses `--gold-text: #d4b47a`, which meets WCAG AA contrast requirements on all dark backgrounds in the design. Decorative borders and lines use a separate `--gold-deco: #b5955a` variable and are never used for text.

| Text color | Background            | Contrast ratio | WCAG level |
| ---------- | --------------------- | -------------- | ---------- |
| `#d4b47a`  | `#131109` (page bg)   | 6.2:1          | AA         |
| `#d4b47a`  | `#1c1a14` (card bg)   | 5.5:1          | AA         |
| `#f0ebe3`  | `#131109` (page bg)   | 13.8:1         | AAA        |
| `#c4bdb0`  | `#131109` (page bg)   | 9.1:1          | AAA        |
| `#131109`  | `#c9a05a` (button bg) | 4.6:1          | AA         |

---

## Contact

Instagram: [@miss.molly.creations](https://www.instagram.com/miss.molly.creations/)
