# Website release handoff

> Historical website handoff from 19 October 2026. The site is now published through GitHub Pages. For the 20 October Unity privacy reconciliation, resolved integration facts and remaining approval/device checks, use [PRIVACY_REVIEW.md](PRIVACY_REVIEW.md) and [PRIVACY_VALIDATION.md](PRIVACY_VALIDATION.md). Earlier statements below about an absent Unity handoff or pre-publication status are superseded.

Prepared: **19 October 2026**. Website: **Legitimately Fishy Games**. Game: **Kitchen Chaos: Idle Cooking**.

**Status:** the static website is technically ready to deploy with its privacy policy explicitly marked as a draft. Local validation passed. No GitHub Pages deployment has been performed or verified as part of this handoff. The final policy is not ready for AdMob: it still awaits the Unity project's `PRIVACY_HANDOFF_WEBSITE.md` and the outstanding review decisions. Approved branding is not a publication blocker.

## Pages and shared files

- `/index.html`: studio homepage, typographic studio name and accurate game/development information.
- `/games/kitchen-chaos/index.html`: text-based game page for the first closed-testing milestone; no invented gameplay screenshots and no working Google Play link.
- `/games/kitchen-chaos/privacy.html`: readable public HTML privacy draft with the supplied contact, **mati4193.004@gmail.com**, and clearly identified final-build questions.
- `/404.html`: consistent missing-page screen with domain-root links suitable for GitHub Pages.
- `assets/css/styles.css`: shared responsive styles, maintainable color/font variables, keyboard focus and reduced-motion support.
- `assets/js/site.js`: minimal mobile navigation enhancement; no analytics or advertising integration.
- `.nojekyll`: plain static publishing; no local build or backend.
- `README.md`: editing, asset integration and safe publication instructions.
- `PRIVACY_REVIEW.md`: app/release facts and decisions that must be confirmed before policy approval.

## Corrections and removed material

- Removed `assets/images/kitchen-concept.webp`, the generated miniature-kitchen concept image. It was not evidence of the real game's appearance.
- Removed `assets/images/favicon.svg`, the unapproved fish studio mark, and removed the fish/mascot symbol from the shared SVG sprite and page decoration.
- Removed the screenshot placeholder cards and image-led game presentation. The game is presented with text and generic interface icons, without replacement game art.
- Removed art-provenance/generation instructions that no longer describe shipped assets.
- Updated the public copy around the actual development/first-closed-test status and confirmed gameplay. No release date, available download, review, testimonial or player statistics are supplied or invented.

The studio name is temporarily typographic. The official octopus branding package and approved gameplay screenshots can be added when provided, following `README.md`. No generated logo, mascot or substitute screenshot is required or approved. Basic layout and publishing do not depend on those future assets.

## Release scope and privacy readiness

The current scope is the **first closed test**: idle resource production, connected farms/stations, recipes, upgrades, managers and random manager boxes using earned in-game currency, local saves and offline progression. Optional local notifications, AdMob rewarded ads and UMP are intended for that milestone, subject to the final-build handoff. **Real-money purchases are not required for this milestone and are not presented as currently available.**

The separate future production milestone plans Google Play Billing diamond packs and purchased diamonds usable for random manager boxes. Purchase processing, verification/recovery and applicable odds disclosures need their own implementation and policy review before that release.

The user-supplied audit reports local JSON saves, settings, progression, manager/currency/loot-box state, local backups and migration copies, and optional quest notifications. It found no developer-operated account/cloud-save server or actual Google Play Billing integration, and identified older Unity LevelPlay/Unity Ads dependencies requiring replacement. Those are **pre-integration audit findings, not proof of the final Android build**.

The privacy draft therefore cannot yet be represented as final for AdMob or Google Play. Before approval:

1. Obtain `PRIVACY_HANDOFF_WEBSITE.md` from the Unity game chat. Confirm the actual shipped dependencies and that legacy ad integrations are removed; match disclosures to the final AdMob and UMP versions/configuration and any remaining providers.
2. Verify actual data handling, local storage/backups/migration copies, Android-managed backup or device-transfer behavior, notifications and deletion effects. Do not imply that New Game or uninstall deletes every copy.
3. Confirm audience, children's and teenagers' handling, regional consent/ad settings and the implemented way to revisit applicable privacy options. A proposed 13+ audience does not settle every age requirement.
4. Resolve the remaining retention, security, international processing, rights-request and support-email handling questions in `PRIVACY_REVIEW.md`. Confirm the supplied privacy address is monitored; do not invent a company registration or physical address.
5. Reconcile the policy, actual app, Google Play declarations and AdMob configuration; approve the policy, remove resolved draft/uncertainty notices and set a genuine effective date.

The website introduces no studio tracking/advertising scripts or third-party widgets. Hosting-provider visitor processing and voluntarily emailed information must remain distinguished from studio-added website tracking. There is no basis to claim that the entire Android app processes no personal information.

## Publishing and AdMob handoff

Existing repository: <https://github.com/legitimatelyfishygames/legitimatelyfishygames.github.io>.

The source came from a ZIP and is not assumed to be a Git checkout. Use the beginner-friendly **README → Publish through the existing GitHub repository** procedure: upload the **inner website root's contents**, including `.nojekyll`, to a normal update branch in the existing repository; remove only known superseded artwork if it exists remotely; review the pull-request diff and merge normally. Do not initialize conflicting history, create a replacement repository, force-push or put tokens in source files.

Select **Settings → Pages → Deploy from a branch**, the actual branch containing the approved files (usually `main` if that branch exists), and **/(root)**. Wait for the corresponding Pages workflow in **Actions** to succeed. Then check:

- Homepage: <https://legitimatelyfishygames.github.io/>
- Game: <https://legitimatelyfishygames.github.io/games/kitchen-chaos/>
- **Exact intended policy URL: <https://legitimatelyfishygames.github.io/games/kitchen-chaos/privacy.html>**

Verify HTTPS and all three pages in a signed-out/private browser; test the policy on a phone with no login or cookie gate. Check links, styles and a missing URL. A local preview is not deployment evidence.

The URL is ready to enter into AdMob only when the **final-build handoff, policy approval, outstanding review items and successful live access checks** are all complete. Completing the branding package is not one of these gates.

## Validation record

Local checks completed on **19 October 2026**:

- All four HTML pages passed the static audit. All **84 local references**, including **39 fragment references**, resolve. The **36 IDs** are unique and **14 ARIA references** have valid targets. Each page has one H1, language and viewport metadata; heading order and HTML nesting passed.
- `node --check assets/js/site.js` passed. No raster assets, image/video/iframe elements, unapproved logos, external or inline scripts, or working store links remain. The shared JavaScript is local.
- All four pages were tested at **320, 390, 768 and 1280 pixels**: **16 layout checks**, with no horizontal overflow. The desktop homepage and mobile game/privacy layouts were visually reviewed.
- Mobile navigation was followed from 404 to the game and then the privacy policy. The menu closes after navigation; Escape closes it and returns focus to the menu button.
- The policy has **15 sections**, a clear draft notice and **three exact `mailto:` links** using `mati4193.004@gmail.com`. No email was sent; these checks do not establish mailbox deliverability or monitoring.
- Browser warning/error logs were empty during testing. Pages and assets returned HTTP 200 through the local Python preview server.

These are local website checks. No Git operations or actual deployment were performed. GitHub Pages' custom-404 mapping, public HTTPS access, signed-out access and access on an actual phone remain **post-deployment checks**. A locally readable draft does not satisfy the remaining final-policy approval gates.
