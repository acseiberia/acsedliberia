# ACSED CMS Setup Checklist

## 1. Create accounts
- GitHub: https://github.com/signup
- Netlify: https://app.netlify.com/signup

## 2. Upload files to GitHub (phone-friendly)
1. Download and unzip `acsed-github-netlify.zip`.
2. In GitHub, create a new repository named `acsed-official-website`.
3. Set it to **Public** only if you are comfortable with the source files being visible. Do not put private data or secrets in the repository.
4. Use **Add file → Upload files** and upload the contents of the unzipped folder (upload the files and folders inside it, not the ZIP itself).
5. Commit the files to the `main` branch.
6. Open `admin/config.yml` and edit it. Replace `YOUR-GITHUB-USERNAME` with your exact GitHub username, then commit the change.

## 3. Deploy on Netlify
1. Sign in to Netlify.
2. Select **Add new project → Import an existing project**.
3. Choose GitHub and authorize Netlify.
4. Select `acsed-official-website`.
5. For this static HTML site, leave build command empty and use `.` as publish directory if prompted.
6. Select Deploy. Netlify should create a public site address ending in `netlify.app`.

## 4. Configure CMS login
The CMS page at `/admin/` is not securely connected until authentication is configured. Decap CMS GitHub backend docs:
https://decapcms.org/docs/github-backend/

Decap's GitHub backend requires an authentication flow. The old Netlify Identity/Git Gateway setup is deprecated for new configurations; do not assume it will work for a new site. Choose a currently supported provider and follow its current setup guide. Never paste secrets into `admin/config.yml` or public repository files.

## 5. Verify before publishing
- Open the public Netlify site.
- Open `/admin/`.
- Confirm authentication works before entering content.
- Test a draft article and an event.
- Check that the published content appears on the public website. This starter needs an additional content-rendering/build step to automatically display markdown content on the homepage.

## Need help?
Proceed one step at a time. Keep your GitHub username handy, but do not share your password or secret tokens in chat.
