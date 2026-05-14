# Shashank Walke — Personal Portfolio

**Live site:** [shashank8walke.github.io](https://shashank8walke.github.io)

M.S. Computer Science student at NC State (4.0 GPA · Tau Beta Pi) · 2× MLH Hackathon Winner · Former SWE at Veritas Technologies and AI/ML Intern at NetApp.

---

## What's Inside

| Section | Content |
|---|---|
| Hero | Typewriter roles, resume download, constellation background |
| About | Bio, stats (GPA, experience, awards, research) |
| Skills | 6×6×6×6 animated skill bars across GenAI, ML, Systems, Cloud |
| Experience | NCSU Thesis · NetApp AI/ML Intern · Veritas SWE (×2) |
| Education | NC State M.S. CS · Walchand College B.Tech IT |
| Projects | 4 GenAI + 5 Systems/Engineering projects |
| Awards | 2× MLH wins · Tau Beta Pi · Veritas recognition · ESA 2026 research |
| Contact | Social links + contact form |

## Tech Stack

Pure static site — no framework, no build step.

- HTML5 · CSS3 (custom properties) · Vanilla JS (ES6+)
- Bootstrap 5.3 · Font Awesome 6.5 · AOS · Typed.js · Particles.js
- Hosted on **GitHub Pages** (auto-deploys on push to `main`)
- Analytics via **GoatCounter** (privacy-first, no cookies)

## Local Preview

No build step needed — just open the file:

```bash
# Clone
git clone https://github.com/shashank8walke/shashank8walke.github.io.git
cd shashank8walke.github.io

# Open directly in browser
open index.html         # macOS
start index.html        # Windows
xdg-open index.html     # Linux
```

## Adding a Project

Find the relevant projects row in `index.html` and add:

```html
<div class="col-md-6 col-lg-3" data-aos="fade-up">
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
    <a href="https://github.com/shashank8walke/REPO-NAME" class="proj-link" target="_blank" rel="noopener">
      <i class="fab fa-github me-1"></i> View on GitHub →
    </a>
  </div>
</div>
```

See [`CLAUDE.md`](./CLAUDE.md) for full instructions (adding roles, swapping resume, updating courses).

## Contact

- Email: [shashank8walke@gmail.com](mailto:shashank8walke@gmail.com)
- LinkedIn: [linkedin.com/in/shashank8walke](https://www.linkedin.com/in/shashank8walke/)
- GitHub: [github.com/shashank8walke](https://github.com/shashank8walke)

---

*Built with HTML · CSS · JS · Hosted on GitHub Pages*
