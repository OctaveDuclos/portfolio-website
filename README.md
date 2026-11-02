# Octave Duclos — portfolio website

A clean, responsive portfolio for renewable energy analytics, AI, and automation. Built with plain HTML, CSS, and JavaScript. No installation or build required.

## Edit the site

Most changes happen in **content.json**. In GitHub, open the file, click the pencil, make changes, and commit to `main`. Keep commas and quotation marks valid JSON. The site updates through GitHub Actions.

- **Introduction:** edit `headline`, `intro`, and `about`.
- **Contact details:** edit `email`, `phone`, `linkedin`, and `github`.
- **Projects:** edit or duplicate an object in `projects`. Give every project a unique `id` using lowercase letters and hyphens. The first three appear on Home; all appear on Portfolio. Each project has `category`, `title`, `summary`, `context`, `work`, `result`, and `tags`. Use category `AI & automation` for the AI filter; other categories appear under Energy & analytics.
- **Additional work:** edit `additional`.
- **Resume experience and education:** edit `experience`, `education`, and `skills`.
- **Photo:** upload `assets/portrait.jpg`. The placeholder automatically switches to your image. Use a portrait or square crop. Update the alt text in `assets/site.js` if needed.
- **Resume PDF:** upload your finalized public resume as `assets/Octave_Duclos_Resume.pdf`, then change `resumeUrl` from `null` to `"./assets/Octave_Duclos_Resume.pdf"`. Until then, the resume page shows a clear placeholder and an editable experience summary.
- **Colors and typography:** edit the variables at the top of `assets/style.css`.
- **Personal page:** intentionally not implemented. When ready, add a page and add its navigation link to each HTML file.

The unfinished Meta resume and the original portfolio packet are intentionally not included in this public repository. No confidential source images or proprietary model files are included. Review project wording and metrics before sharing externally.

## GitHub Pages

The workflow `.github/workflows/pages.yml` deploys every push to `main`.

If the first run reports that Pages is unavailable or cannot be created, open **Settings → Pages → Build and deployment → Source**, select **GitHub Actions**, and run the workflow again from **Actions → Deploy portfolio to GitHub Pages → Run workflow**.

Expected address once deployed: https://octaveduclos.github.io/portfolio-website/

## Local preview

Run `python3 -m http.server 8000` from this directory, then open http://localhost:8000. Use a local web server rather than opening HTML directly so the browser can load `content.json`.
