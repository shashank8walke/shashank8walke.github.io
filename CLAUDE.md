# CLAUDE.md — Coding Standards for shashank8walke.github.io

## Stack
Pure static site. No npm, no build process.
HTML5 · CSS3 with custom properties · Vanilla JS (ES6+) · Bootstrap 5.3 via CDN

## File Layout
```
shashank8walke.github.io/
├── index.html              (single-file portfolio)
├── CLAUDE.md               (this file)
├── README.md
└── assets/
    ├── css/style.css
    ├── js/main.js
    ├── files/resume.pdf    (AI-focused resume; swap as needed)
    └── images/
        └── profile/
            └── profile_image.HEIC   (convert to profile.jpg — see below)
```

## Adding a GitHub Link to a Project
Find the project's `<span class="proj-link private">` and replace it with:
```html
<a href="https://github.com/shashank8walke/REPO-NAME" class="proj-link" target="_blank" rel="noopener">
  <i class="fab fa-github me-1"></i> View on GitHub →
</a>
```

## Adding a New Project
Copy this block and paste it inside the correct `.row.g-4` in `index.html`:
```html
<div class="col-md-6 col-lg-3" data-aos="fade-up" data-aos-delay="0">
  <div class="dark-card proj-card">
    <div class="proj-icon-circle" style="--icon-color:#a78bfa; --icon-r:167; --icon-g:139; --icon-b:250;">
      <i class="fas fa-ICON-NAME"></i>
    </div>
    <div class="proj-tags">
      <span class="tag">Tag1</span>
      <span class="tag">Tag2</span>
    </div>
    <h3 class="proj-title">Project Title</h3>
    <p class="proj-desc">Short description of what it does and why it matters.</p>
    <!-- Replace the span below with an <a> once the GitHub repo is public -->
    <span class="proj-link private"><i class="fas fa-lock me-1"></i> Private — Coming Soon</span>
  </div>
</div>
```
- For GenAI projects: add inside the first `.row.g-4` (after the GenAI category label)
- For Engineering projects: add inside the second `.row.g-4`
- Update the count in the `<span>` inside `.projects-category-label`
- Pick an icon name from fontawesome.com (free tier)
- Pick a color: purple `#a78bfa`, blue `#60a5fa`, pink `#f472b6`, green `#34d399`, orange `#fb923c`

## Adding a New Experience Role
Copy an `.alt-timeline-item` block. Use `left` for odd items (1st, 3rd) and `right` for even items (2nd, 4th).
Add newer roles at the top.

## Swapping the Profile Photo
1. Convert `assets/images/profile/profile_image.HEIC` to JPEG using squoosh.app or macOS Preview (Export → JPEG)
2. Save as `assets/images/profile/profile.jpg`
3. In `index.html`, find the `about-photo-frame` div and replace:
   ```html
   <!-- FROM: -->
   <div class="about-photo-initials">SW</div>
   <!-- TO: -->
   <img src="assets/images/profile/profile.jpg" alt="Shashank Walke" class="about-photo-circle">
   ```

## Swapping the Resume
Drop the new PDF at `assets/files/resume.pdf` — the download button and navbar link update automatically.

## CDN Versions (pinned)
| Library      | URL |
|--------------|-----|
| Bootstrap CSS | `https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css` |
| Bootstrap JS  | `https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js` |
| Font Awesome  | `https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css` |
| AOS CSS       | `https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css` |
| AOS JS        | `https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js` |
| Typed.js      | `https://cdnjs.cloudflare.com/ajax/libs/typed.js/2.0.12/typed.min.js` |
| Particles.js  | `https://cdnjs.cloudflare.com/ajax/libs/particles.js/2.0.0/particles.min.js` |

## Analytics
GoatCounter account: `shashank` → dashboard at https://shashank.goatcounter.com
Script is placed just before `</body>`.

## GitHub Pages Deployment
- Push to `main` branch → site auto-deploys in ~60 seconds
- Live at: https://shashank8walke.github.io
- No `/docs` folder needed — deploys from root

## Git Commit Style
```
add projects section
fix mobile nav overflow
update resume pdf
```
Lowercase imperative. No ticket numbers needed.
