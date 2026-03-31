# JPI GitHub Pages Starter

This repository is configured as a **project GitHub Pages site** for a repo named `jpi`.

## Expected live URL

`https://YOUR-USERNAME.github.io/jpi/`

## Important `_config.yml` values

- `baseurl: "/jpi"`
- `url: "https://YOUR-USERNAME.github.io"`

Before publishing, replace `YOUR-USERNAME` in `_config.yml` with your real GitHub username.

## Recommended GitHub setup

1. Create a new repository named `jpi`.
2. Upload all files from this folder to the repository root.
3. Commit to the default branch (typically `main`).
4. In GitHub, go to **Settings -> Pages**.
5. Under **Build and deployment**, set:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main`
   - **Folder:** `/ (root)`
6. Save.

GitHub Pages should publish the site at:

`https://YOUR-USERNAME.github.io/jpi/`

## Editing content

- Home page: `index.md`
- About page: `about.md`
- Editorial board: `editorial-board.md`
- Submissions: `submissions.md`
- Policies: `policies.md`
- Contact: `contact.md`
- Archives page: `archives.html`
- Issue records: files in `_issues/`
- Shared header/footer: files in `_includes/`
- Layouts: files in `_layouts/`
- Styling: `assets/css/style.css`

## Adding a new issue

1. Add the issue PDF to `assets/pdf/...`
2. Copy one of the files in `_issues/` and update its metadata.
3. Commit and push.

Because `archives.html` loops over the `issues` collection, the new issue should appear automatically.
