# Legitimately Fishy Games website

A static website for **Legitimately Fishy Games** and **Kitchen Chaos: Idle Cooking**, using HTML, shared CSS and minimal vanilla JavaScript. No build step, package manager, paid service or backend is needed.

The game is under development and preparing for its first **closed test**. There is no supplied public Google Play destination. The privacy contact is **mati4193.004@gmail.com**.

**The privacy policy remains a draft.** The Unity engineering handoff of 19–20 October 2026 has been reviewed; its validation AAB is not assumed to be the final candidate. Resolve the remaining decisions and device checks in [PRIVACY_REVIEW.md](PRIVACY_REVIEW.md) before approval for AdMob or Google Play. [PRIVACY_VALIDATION.md](PRIVACY_VALIDATION.md) records this revision's website checks. The website is published through GitHub Pages; revised local files still require review, merge and deployment.

## Website root and structure

The ZIP was extracted into a second folder with the same name. The **inner** `legitimatelyfishygames.github.io-main` folder, containing this README and `index.html`, is the website root. Publish its **contents**, not the enclosing folder.

```text
index.html                         Studio homepage
games/kitchen-chaos/index.html     Closed-test game information
games/kitchen-chaos/privacy.html   Privacy policy draft
404.html                           Missing-page screen
.nojekyll                          Serve plain static files without Jekyll processing
assets/css/styles.css              Shared styles, CSS variables and responsive layouts
assets/js/site.js                  Navigation enhancement
assets/images/icons.svg            Generic interface icons; no studio mascot
PRIVACY_REVIEW.md                  Questions requiring app/release confirmation
WEBSITE_RELEASE_HANDOFF.md         Website status and publication handoff
README.md                          Editing and publishing instructions
```

Intended public URLs after deployment:

- Studio: <https://legitimatelyfishygames.github.io/>
- Game: <https://legitimatelyfishygames.github.io/games/kitchen-chaos/>
- Privacy: **<https://legitimatelyfishygames.github.io/games/kitchen-chaos/privacy.html>**

The privacy policy is ordinary HTML with no sign-in or cookie gate. HTTPS access still needs to be verified on the deployed site.

## Preview locally

From the website root, run the following if Python is installed:

```powershell
python -m http.server 8000
```

Open <http://localhost:8000/>. Stop the preview with `Ctrl+C`. Python is optional for preview only; hosting needs no Python. You can also open `index.html` directly for a quick look, but a server better matches hosted navigation.

A local server may show its own error screen for missing addresses. Open `/404.html` to inspect this site's custom page, then test an invented missing address on GitHub Pages after deployment.

## Update game information

Edit the HTML directly. Keep the homepage and game page consistent with the actual app, its handoff and the current release milestone.

- **Closed testing:** core idle production, local saves and offline progression, managers and random manager boxes obtained with earned currency. Direct Google Mobile Ads/UMP and optional local notifications are implemented according to the Unity handoff; production advertising remains gated pending audience review and device validation. Real-money purchases are not required for this milestone and are not advertised as available.
- **Future public release:** Google Play Billing diamond packs, purchased diamonds usable for random manager boxes, and related purchase/odds handling are a separate planned milestone. Do not turn these plans into current closed-test claims.
- Keep the development/closed-test status until it changes. Add a store link only when the actual valid destination is supplied. Do not invent a release date, review, download count, cloud save or player account.
- Recheck the privacy policy when app SDKs, backups, purchases, audience, providers or consent controls change. A source audit of the older Unity project does not prove the final APK's behavior.
- To add another game, create `games/<game-slug>/index.html`, reuse the shared CSS and JavaScript, and add its own accurate privacy information and navigation.

## Add approved screenshots and branding later

The current design uses text and generic interface icons. Generated kitchen art, the unapproved fish mark/mascot and screenshot placeholder cards have been removed. No logo or screenshot is needed to publish the text-based website.

When **approved** assets are supplied:

1. Put genuine game screenshots or the official branding package in `assets/images/`. Use clear file names and optimized image sizes. Do not generate substitute screenshots, mascots or logos.
2. Add screenshots to the game page only when they represent the actual build; include meaningful `alt` text, accurate captions and image `width`/`height`. Check them on a phone.
3. Insert an approved studio logo alongside or in place of the typographic studio name in the headers/footers of all pages. Keep the name accessible to screen readers. Add a favicon link only when an approved favicon exists.
4. Change colors and font families through the `:root` variables near the top of `assets/css/styles.css`. Keep local/system fonts and sufficient contrast. Preserve visible keyboard focus, mobile navigation and reduced-motion behavior.

The website contains no studio-added analytics, ad scripts, tracking cookies or third-party embeds. GitHub Pages may process visitor information for hosting/security; the policy distinguishes that from studio tracking and information voluntarily emailed to the contact address.

## Publish through the existing GitHub repository

Use [legitimatelyfishygames/legitimatelyfishygames.github.io](https://github.com/legitimatelyfishygames/legitimatelyfishygames.github.io). This ZIP may have no `.git` directory. Do **not** run `git init`, create a replacement repository, overwrite remote history, force-push, or put access tokens in website files.

### Browser upload: step by step

1. Sign in to GitHub and open the existing repository above. On **Code**, note the selected branch name (often `main`). Open **Settings → Pages** in another tab and note any existing publishing branch/folder. Use the real branch names you see; do not assume `main` exists.
2. Return to **Code** and open the root of the branch that should receive the site update. Review existing files first; preserve unrelated files and any existing hosting configuration.
3. Choose **Add file → Upload files**. In File Explorer, open the **inner website root**, select its files and the `assets` and `games` folders, and drag those selected contents into the upload area. Do not drag the enclosing `legitimatelyfishygames.github.io-main` folder. Include `.nojekyll`; show hidden files in File Explorer if needed.
4. Check the upload list: `index.html`, `404.html` and the Markdown files belong directly at the root; `games/kitchen-chaos/privacy.html` and `assets/css/styles.css` must keep those paths. Do not upload a ZIP, private Unity files, keys or access tokens.
5. Enter a commit message such as `Update studio website and closed-test privacy draft`. Choose **Create a new branch for this commit and start a pull request**, using a name such as `website-update`, then **Propose changes**. Follow the repository's branch rules if its controls differ.
6. Browser uploads do not delete old files. If this repository already contains the superseded `assets/images/kitchen-concept.webp` or `assets/images/favicon.svg`, open each on your update branch, choose the file's **… → Delete file** control, and commit its deletion to the same update branch. Keep unrelated assets. The updated `icons.svg` replaces the old fish symbol; inspect that diff too.
7. Open the pull request and review **Files changed**. Confirm the correct root paths, intended deletions and privacy draft status. Complete the normal review/merge into the intended publishing branch. This preserves the repository's history.
8. Open **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, choose the branch containing the merged site (usually `main`, if that is its actual name), choose **/(root)**, and click **Save**. Inspect an existing deployment setup before changing it. No custom build workflow is required for these files.
9. Open **Actions** and wait for the Pages build/deployment workflow for the relevant commit to finish successfully. A commit or successful upload alone does not prove that the website is live. If the workflow fails, inspect its error before continuing.
10. Open the three intended public URLs above. In a signed-out/private window, confirm HTTPS, readable content, working navigation and no missing styles. Open the **exact privacy URL on a phone** and confirm it needs neither login nor cookie acceptance. Test an invented missing address to check the 404 page.
11. Submit the privacy URL to AdMob/Google Play **only after** both the policy approval gates below and these live checks pass. Publishing a visible draft does not make it a finalized policy.

GitHub's official instructions cover [uploading files](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository) and [choosing the Pages publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

### Authenticated clone alternative

Clone the **existing** repository into a separate folder using GitHub Desktop or normal authenticated Git. Inspect its branch and current files, create a working branch, and copy this website root's contents into it without removing its `.git` directory or unrelated files. Remove the known superseded artwork there if present. Review `git status`, `git diff` and the staged diff; commit only intended changes, push the working branch normally and open a pull request. Reconcile remote changes normally. Do not force-push or initialize the ZIP as a competing history. Then use steps 8–11 above.

## Gates before entering the privacy URL into AdMob

- Use the reviewed Unity handoff and obtain final-candidate evidence; reconcile the policy with that Android build and configuration. See resolved findings and remaining device/developer checks in `PRIVACY_REVIEW.md`.
- Complete [PRIVACY_REVIEW.md](PRIVACY_REVIEW.md), particularly audience/teen/child handling, SDK disclosures, consent/privacy controls, backup/deletion limitations, rights and support handling. Use the supplied real contact; verify it is monitored.
- Approve the app-specific policy, resolve public uncertainty notices and set an actual effective date only at approval. Keep future paid diamonds and paid random-box use separate from the current closed-test scope.
- Confirm the exact HTTPS policy URL works publicly, signed out and on a mobile browser, after the successful deployment. Enter that reviewed URL into the relevant consoles and app links.
