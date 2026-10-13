# Chanora website

One-page bilingual (French / English) site for Chanora. Static HTML, no build step, ready for GitHub Pages.

## Files

- `index.html` — the whole site (styles and script included)
- `img/` — images, logos and favicons
- `.nojekyll` — tells GitHub Pages to serve the files as they are

## Publish on GitHub Pages

1. Create a new repository on GitHub, for example `chanora-website`.
2. Upload everything in this folder (including `.nojekyll`) to the repository's main branch.
3. In the repository, go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
4. After a minute or two the site is live at `https://<your-username>.github.io/chanora-website/`.

## Use your own domain (optional)

To serve the site at `www.chanora.co`:

1. In **Settings → Pages → Custom domain**, enter `www.chanora.co` and save. GitHub adds a `CNAME` file to the repository.
2. At your domain registrar, add a `CNAME` record: `www` → `<your-username>.github.io`.
3. Back in **Settings → Pages**, tick **Enforce HTTPS** once it becomes available.

## Contact form

The form sends requests to **mo@chanora.co** through FormSubmit (formsubmit.co), a free service that works with static sites.

- **First submission:** FormSubmit emails an activation link to mo@chanora.co. Click it once; after that, every request arrives in the inbox.
- **Hide the email address (recommended):** after activation, FormSubmit sends a random alias string. Replace `mo@chanora.co` in `index.html` (it appears in the form's `action` and in the script) with that string so the address is not visible in the page source.
- Spam protection uses a hidden "honeypot" field.

## Editing content

All text is in `index.html`. Each text appears twice: `lang="fr"` for French and `lang="en"` for English. Change both.
