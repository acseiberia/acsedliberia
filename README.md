# ACSED Official Website — GitHub + Netlify + Decap CMS

This package contains the ACSED public website, logo, CMS admin page, and starter configuration.

## Files
- `index.html` — public-facing homepage
- `images/acsed-logo.jpeg` — supplied ACSED logo
- `admin/index.html` — Decap CMS interface loader
- `admin/config.yml` — CMS collections and GitHub backend placeholder
- `content/news/`, `content/events/`, `content/publications/` — content folders
- `netlify.toml` — Netlify configuration
- `CMS-SETUP.md` — deployment and CMS setup guide

## Important: CMS login is not configured yet
Before the `/admin/` interface can publish content, you must:
1. Create a GitHub account.
2. Upload these files to a GitHub repository named `acsed-official-website`.
3. Replace `YOUR-GITHUB-USERNAME` in `admin/config.yml` with your GitHub username.
4. Deploy the repository to Netlify.
5. Configure a supported authentication provider for Decap CMS. Follow the current Decap CMS GitHub backend documentation:
   https://decapcms.org/docs/github-backend/

Never put a password, GitHub access token, OAuth client secret, or other secret in the repository.

## Deploy to Netlify
1. Sign in to Netlify.
2. Choose **Add new project** → **Import an existing project**.
3. Connect GitHub and select `acsed-official-website`.
4. For this plain HTML site, leave the build command blank and set the publish directory to `.` if Netlify requests it.
5. Deploy. Netlify will provide a public `netlify.app` address.

Netlify documentation: https://docs.netlify.com/start/quickstarts/deploy-from-repository/

## Content behavior note
This starter config defines CMS content collections and stores markdown files in `content/`. A static HTML page does not automatically render those markdown entries on its homepage. The CMS will store and manage content, but to show every new article/event automatically on the public homepage, a build/render step or content API integration must be added. This starter is a base for the CMS configuration, not a claim that login or live content rendering is already working.

## Styling
The site uses ACSED red, green, and white, Anton for headings, and bold Times New Roman for body copy. Anton is loaded from Google Fonts when internet access is available; fallback fonts are included.
