# Mentoria Hub

Static website prototype with:
- first-step registration with student/admin role choice
- protected admin panel
- opportunities catalog
- SAT and IELTS courses with practice tasks
- college list with 200 universities
- courses and lesson progress
- roadmap and dashboard
- Marsula mascot and AI assistant
- Figma-ready iPhone 16 prototype frames
- uploaded SAT, IELTS, vocabulary, and university ranking PDF resources
- English, Russian, and Kazakh UI translations

## Demo Login Rules

Students can:
- register and log in
- access their student dashboard
- complete the 20-question career orientation after registration
- save opportunities
- use courses, roadmap, dashboard, and Marsula AI
- practice IELTS Listening, Reading, Writing, Speaking, and vocabulary modules
- browse the college list and build a shortlist

Admins can:
- enter the protected Admin page after registration/login
- open the Admin page
- create opportunities
- delete opportunities
- view registered site accounts

To create an admin account in this demo, choose `Site admin` during registration and enter:

```text
MENTORIA-ADMIN
```

This is prototype-level frontend access control. For a real product, move accounts, roles, and AI keys to a backend such as Firebase, Supabase, or a custom server.

## Publish On GitHub Pages

1. Create a new GitHub repository.
2. Upload everything from this folder:
   - `index.html`
   - `styles.css`
   - `app.js`
   - `universities.js`
   - `figma-iphone-prototype.html`
   - `assets/`
   - `README.md`
3. Go to repository `Settings`.
4. Open `Pages`.
5. Under `Build and deployment`, choose:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
6. Save.
7. Wait for GitHub Pages to publish the site.

Your site URL will look like:

```text
https://YOUR_USERNAME.github.io/YOUR_REPOSITORY_NAME/
```

## Files

- `index.html` - page structure
- `styles.css` - design and responsive layout
- `app.js` - navigation, account logic, roles, admin panel, translations, Marsula AI
- `universities.js` - top 200 university data used by the Colleges page
- `figma-iphone-prototype.html` - iPhone 16 frame prototype for rebuilding/animating in Figma
- `assets/` - logo, mascot images, videos, dashboard preview
- `assets/files/` - uploaded SAT, IELTS, vocabulary, and university PDFs

## AI

Marsula AI uses Gemini through:

```text
https://generativelanguage.googleapis.com/v1beta/models/gemini-flash-latest:generateContent
```

Do not commit a real Gemini API key to GitHub. The site has an AI settings field where you can paste a key locally in the browser and click `Save AI`; it is saved only on that device in `localStorage`. For a real launch, move the key to a backend/proxy so students cannot see it in browser code.
