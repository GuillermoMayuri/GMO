# GGLLC

A small web project based on the index.html from the GMO repository. This README explains how to run, customize, and publish the site. Replace or update any sections below after you provide the exact GMO repo link so attribution and licensing can be completed accurately.

## Table of Contents
- [About](#about)
- [Preview](#preview)
- [Files of interest](#files-of-interest)
- [Prerequisites](#prerequisites)
- [Run locally](#run-locally)
- [Developing and customizing](#developing-and-customizing)
- [Publishing](#publishing)
- [Licensing & attribution](#licensing--attribution)
- [Contributing](#contributing)
- [Contact](#contact)

## About
GGLLC is a lightweight static web project that starts from the `index.html` in the GMO repository. It is intended to serve as a simple website (landing page or prototype) that you can edit, style, and extend.

## Preview
(Replace this section with a screenshot or link to a live demo after you deploy.)

## Files of interest
- index.html — main page (origin: GMO repository)
- assets/ — (optional) CSS, JS, images used by index.html
- README.md — this file
- LICENSE — add the appropriate license (see Licensing & attribution)

## Prerequisites
You only need a modern web browser to view the site. For local development, a minimal static file server is helpful:
- Node.js (optional) or
- Python 3 (optional) or
- Any static hosting (Netlify, Vercel, GitHub Pages, etc.)

## Run locally

Simple options:

1) Open directly
- Double-click `index.html` or open it in your browser.

2) Using Python (recommended for relative asset paths)
```bash
# From the project root
python -m http.server 8000
# Then open http://localhost:8000 in your browser
```

3) Using Node (http-server)
```bash
npm install -g http-server
http-server -p 8000
# Then open http://localhost:8000
```

## Developing and customizing
- Edit `index.html` to change text, links, and structure.
- Place CSS and JS files under an `assets/` folder (or follow the existing structure from GMO).
- Keep assets referenced by relative paths for simple hosting.
- When making larger changes, consider creating feature branches:
```bash
git checkout -b feat/update-homepage
```

## Publishing
Choose any static host:

- GitHub Pages
  - Create a repo (or push to an existing one).
  - Push to the `gh-pages` branch or enable Pages from `main`/`docs`.
  - For a quick publish:
    ```bash
    git init
    git add .
    git commit -m "Initial commit for GGLLC"
    git remote add origin git@github.com:<your-user>/GGLLC.git
    git push -u origin main
    ```
  - Enable GitHub Pages in repo settings.

- Netlify / Vercel
  - Connect your GitHub repo, set build to "None" (static) or use simple build step, and deploy.

- Static Docker (optional)
  ```bash
  docker run --rm -p 8080:80 -v "$PWD":/usr/share/nginx/html:ro nginx:alpine
  ```

## Licensing & attribution
This project is based on `index.html` from the GMO repository. Before publishing, confirm the GMO repository license and include required attribution or license files here.

- If the GMO content is licensed (MIT/Apache/GPL/etc.), copy or link the LICENSE file and add attribution in this README.
- If unsure, provide the GMO repo URL and I will fetch the license and recommend the correct attribution text.

## Contributing
- Fork the repo
- Create a branch: `git checkout -b feat/my-change`
- Commit and open a pull request
- Add a short description of your changes and any testing steps

Optionally add:
- CONTRIBUTING.md
- CODE_OF_CONDUCT.md

## Contact
Maintainer: GuillermoMayuri  
Email: (add your contact email here)

## Next steps / Notes
- Provide the GMO repository link (owner/repo or the blob URL to `index.html`) and I will:
  - Fetch the `index.html`
  - Extract title, meta description, and assets list
  - Add screenshot/sample preview and exact license/attribution text
  - Update this README with concrete usage examples and any special setup the file requires
