# Ekoparty 2026 session companion

A lightweight, mobile-first static landing page for **From one identity to full
compromise**, Cloud Security Village. Built with HTML, CSS, and a minimal
JavaScript configuration constant. No dependencies, build step, analytics, or
external assets. All navigation works with JavaScript disabled.

The black canvas, white/lilac title, thin cyan/blue rules, and double-outline
cyan/purple/green takeaway panels follow the presentation's visual language.
No source-deck screenshots or non-public presentation content are embedded.

## Files

```text
index.html
styles.css
script.js
README.md
assets/
  README.md
  Ekoparty_2026_From_One_Identity_to_Full_Compromise.pdf  (add before publishing)
```

## Before publishing

1. The feedback URL is configured as
   `https://forms.cloud.microsoft/r/PJTAnU4Kmt`. To change it later, find the
   comment `FEEDBACK_URL` in `index.html` and update the `href` on
   `id="feedback-link"`. This is the **only URL value to edit**.
   The named `FEEDBACK_URL` constant in `script.js` reads it directly.
   Confirm the form accepts responses from your intended audience.
2. Export and review a public-only deck, then put it in
   `assets/Ekoparty_2026_From_One_Identity_to_Full_Compromise.pdf`.
   Do not simply publish the original presentation. Exclude notes, hidden
   slides, internal-only information, internal URLs, private customer data,
   and screenshots that are not intended for publication.
3. Test both the PDF download and the form on a phone before printing the QR.
   The download cannot work until the PDF is present.

See [assets/README.md](assets/README.md) for optional photos and favicon guidance.

## Preview locally

For a quick visual preview, open `index.html` directly in a browser. Relative
styles, links, and the JavaScript file work without a server. Add the PDF first
to test its download.

For an HTTP preview, use VS Code's **Live Preview** extension if available:
open this folder, open `index.html`, and run **Live Preview: Show Preview**.
No project dependencies or build tools are needed.

Check 390px mobile, 768px tablet, and 1440px desktop widths using the browser's
responsive developer tools. Also check keyboard Tab navigation, reduced motion,
and the page with JavaScript disabled.

## Create a repository and push

1. Sign in to GitHub and select **New repository**.
2. Choose a stable name, for example `ekoparty-2026`. Use a public repository
   for the simplest GitHub Pages setup. Do not initialize it with a README,
   license, or gitignore when pushing the existing files below.
3. From PowerShell in this folder:

   ```powershell
   git init
   git branch -M main
   git add index.html styles.css script.js README.md assets/README.md
   # Run this only after the reviewed public PDF exists:
   git add assets/Ekoparty_2026_From_One_Identity_to_Full_Compromise.pdf
   git commit -m "Publish Ekoparty session companion"
   git remote add origin https://github.com/USERNAME/REPOSITORY.git
   git push -u origin main
   ```

   Replace `USERNAME` and `REPOSITORY`. If Git requests an identity, configure
   your own name and email. Authenticate using GitHub's supported Git login
   flow; do not put credentials into the site.

   **Do not run `git add .` in this workspace.** It also contains the original
   PDF, PowerPoint, and other documents that are not part of the public site.
   Stage only the explicitly listed site files and approved public assets.

## Enable GitHub Pages

In your repository, select:

**Settings → Pages → Deploy from a branch → main → / (root) → Save**

Wait for the deployment to finish. The project site's final URL should be:

```text
https://USERNAME.github.io/REPOSITORY/
```

All site asset paths are relative, so they work under the repository subpath.
No custom-domain, absolute-root path, or server-side configuration is needed.

## QR destination and future updates

**The QR code must point to the GitHub Pages landing page, not directly to
the PDF or feedback form.** Use the final HTTPS URL above and include the
trailing slash.

Keep your GitHub username, repository name, and Pages destination stable.
You can replace the PDF under the same filename, change the form URL, and
update the page without changing the QR destination.

To update, edit the files, preview the page, stage only the changed public
site files, commit, and push:

```powershell
git add index.html styles.css script.js README.md assets/README.md
# Include this only when the public deck changed:
git add assets/Ekoparty_2026_From_One_Identity_to_Full_Compromise.pdf
git commit -m "Update session companion"
git push
```

GitHub Pages redeploys from `main`. Verify the public page after deployment;
a hard refresh may be needed to see updated cached assets.

## Publication checklist

- PDF filename and capitalization match the download link exactly.
- PDF is approved for public distribution and downloads successfully.
- Forms URL is configured and attendee access is tested.
- All six Microsoft Learn links open the intended documentation in new tabs.
- Keyboard focus is visible and controls are comfortable to tap on mobile.
- No horizontal scrolling at mobile, tablet, or desktop widths.
- QR points to the deployed landing page and has been scanned on a phone.
- Only approved site files and assets are tracked in the public repository.
