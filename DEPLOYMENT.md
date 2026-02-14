# Pickleball & AI Landing Page — Deployment Documentation

## Live URL

**Permanent Public URL:** https://files.manuscdn.com/user_upload_by_module/session_file/93803286/fMBqcJWBHykiBnAa.html

This URL is hosted on Manus CDN and provides permanent, reliable access to the landing page.

## Alternative Deployment Options

### GitHub Repository

The source code is also available in a public GitHub repository:
- **Repository:** https://github.com/BananaMan1985/pickleball-and-ai
- **Branch:** main
- **File:** index.html

While GitHub Pages could not be enabled via CLI due to token permissions, the repository serves as version control and backup.

## Form Backend

The application form submits directly to **Jotform**:
- **Form ID:** 260445552588061
- **Form URL:** https://form.jotform.com/260445552588061
- **Submission Endpoint:** https://submit.jotform.com/submit/260445552588061

### Form Fields

The form collects the following information:
1. **Full Name** (required) — Text input
2. **Email** (required) — Email input
3. **Company Name** (required) — Text input
4. **Membership** (required) — Dropdown with options:
   - Yes — Sagan member
   - Yes — Crane member
   - No — neither
5. **Why do you want to attend?** (required) — Textarea
6. **What are you hoping to build or solve with AI?** (required) — Textarea

All submissions are automatically stored in Jotform and can be viewed at: https://www.jotform.com/myforms/

## Design Specifications

### Theme
- **Style:** Dark premium design with gold accents
- **Primary Colors:**
  - Background: #0a0a0a (dark black)
  - Gold accent: #c9a84c
  - Text primary: #e8e4dc (off-white)
  - Text secondary: #9a958c (muted gray)

### Typography
- **Headings:** Playfair Display (serif, elegant)
- **Body:** Inter (sans-serif, clean)

### Key Features
- Fully responsive design (mobile-optimized)
- Smooth scroll navigation
- Fade-in animations on scroll
- Form validation with required fields
- Success message after submission
- Hidden iframe for seamless Jotform integration

## Technical Stack

- **HTML5** with semantic markup
- **CSS3** with custom properties (CSS variables)
- **Vanilla JavaScript** for interactions
- **Google Fonts** for typography
- **Jotform** for form backend and data collection

## File Structure

```
pickleball-and-ai/
├── index.html          # Self-contained landing page (all CSS/JS inline)
├── DEPLOYMENT.md       # This file
└── .git/              # Git repository
```

## Maintenance

To update the landing page:

1. Edit `/home/ubuntu/pickleball-and-ai/index.html`
2. Test locally: `python3 -m http.server 8080`
3. Upload to CDN: `manus-upload-file index.html`
4. Commit to GitHub: `git add -A && git commit -m "Update" && git push`

## Notes

- The CDN URL is permanent and will not expire
- Form submissions go directly to Jotform (no server-side code needed)
- The page is fully static and requires no backend infrastructure
- All assets (fonts) are loaded from Google Fonts CDN
- No external dependencies beyond Google Fonts

## Contact

For form submission inquiries or to view responses, log into Jotform at https://www.jotform.com/
