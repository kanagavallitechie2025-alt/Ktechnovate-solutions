# KTechnovate Solutions Website

A responsive React + Vite website for KTechnovate Solutions, styled around the supplied navy-blue and cyan brand palette.

## Requirements
- Node.js 18+ (Node 20+ recommended)
- npm

## Run locally
1. Extract this folder.
2. Open the folder in VS Code.
3. Open the integrated terminal in the project root.
4. Run:

   ```bash
   npm install
   npm run dev
   ```

5. Open the local URL printed by Vite (usually `http://localhost:5173`).

## Production build
```bash
npm run build
npm run preview
```
The production files are generated in `dist/`.

## Pages included
- Home
- About
- Services
- Projects with working category filters
- Individual project details (`/projects/:id`)
- Contact
- Start a Project / quote inquiry
- Privacy Policy starter
- Terms & Conditions starter
- Custom 404 page

## Brand details
- Company: KTechnovate Solutions
- Email: ktechnovatesolutions@gmail.com
- Working model: Remote-first
- Tagline: Your Ideas | Our Technology | Real Solutions
- Main colors: navy blue, white, cyan

The header uses a text-based logo mark inspired by the supplied logo. Replace the `Logo` component in `src/App.jsx` with an actual image file if you want to use the original logo directly.

## Contact form behavior
The form validates required fields and email formatting, then opens the visitor's default email application with a prefilled message addressed to `ktechnovatesolutions@gmail.com`. It does not store form submissions and is not a server-side contact form. If you want submissions to arrive without the visitor using an email app, connect a form service or build a secure backend endpoint before production.

## Before publishing
- Review the Privacy Policy and Terms pages with a qualified professional and customize them to match your actual business practices and jurisdiction.
- Confirm project descriptions/statuses and update any missing HRMS technology details.
- Add verified GitHub/demo links where available.
- Add a custom domain and update metadata in `index.html`.
- Consider adding a server-side form endpoint and spam protection if using a backend.
- Add `public/robots.txt`, a sitemap, and per-route SEO metadata before production launch if required.

## Suggested deployment
### Netlify
1. Push the project to a GitHub repository.
2. In Netlify, choose **Add new site → Import an existing project**.
3. Select the repository.
4. Build command: `npm run build`
5. Publish directory: `dist`
6. Deploy.

For a React Router single-page app, add a file named `public/_redirects` containing:
```
/* /index.html 200
```
Create the `public` directory if needed.

### Vercel
Import the Git repository into Vercel and use the Vite preset. Build command `npm run build`, output directory `dist`. Configure SPA rewrites if needed.

## Project structure
```
src/
  App.jsx       # Pages, shared layout, forms and routes
  data.js       # Editable services and project content
  main.jsx      # React entry point
  styles.css    # Design system and responsive styles
index.html
package.json
README.md
```
