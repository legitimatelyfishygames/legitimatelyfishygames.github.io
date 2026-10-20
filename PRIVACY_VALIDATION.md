# Privacy revision validation — 20 October 2026

Scope: reconcile the complete Unity `PRIVACY_HANDOFF_WEBSITE.md` (19–20 October) with the existing policy and review checklist. The updated policy remains **DRAFT**, with no effective date or approval for AdMob submission. The source validation AAB is not assumed to be the final Android candidate.

## Website checks completed

- W3C Nu HTML checker, version **26.10.18**, checked the revised policy HTML: **zero errors or warnings** (`messages: []`, language `en`).
- Local structural audit of all **four HTML pages**: correct tag nesting, no duplicate attributes/IDs, **113 local references** resolve (including HTML and SVG fragments), **36 unique IDs** across the pages and valid ARIA targets. Linked policy/review assets exist.
- Headless Microsoft Edge/Playwright tested the revised policy at **320, 390, 580, 581, 768, 1024 and 1280 CSS pixels**: no horizontal overflow or clipped tested text; eager images loaded. An unneeded public package identifier initially overflowed at 320px and was removed from public prose; the exact intended package remains in the review record. All seven widths passed after that correction.
- Policy navigation/assets returned HTTP 200 locally and fragment targets resolved. No page JavaScript errors, failed browser requests or HTTP errors were observed during the successful browser run.
- Basic accessibility checks passed: English language and title; one main landmark and H1; ordered headings; 15 policy sections; named links/buttons; image alt attributes; valid ARIA references; working keyboard skip link; mobile menu expansion and Escape closing with focus returned; working policy contents navigation; reduced-motion transition duration zero. Desktop and mobile screenshots were reviewed. This is a scoped check, not a full assistive-technology or WCAG certification.
- The three contact links remain exactly `mailto:mati4193.004@gmail.com`; no message was sent and mailbox monitoring/deliverability is not established by link checks.
- Shared navigation JavaScript syntax check passed. Branding, fonts, images, CSS, JavaScript and other public HTML pages are unchanged. README privacy guidance and the historical website handoff note now point to the current review instead of treating the supplied Unity handoff as missing.
- Google Mobile Ads disclosure, UMP Unity integration and Android Auto Backup references were rechecked. They support provider/platform explanations; they do not establish the game's actual network behavior.

Local browser and structural validation used workspace-only helper scripts and saved screenshots/JSON reports outside the deployment checkout. The initial sandbox browser/server connection attempts failed; the successful browser run used a local server in the same process. Those setup failures were not counted as passing checks.

## Publication workflow and limits

The working branch is `privacy/unity-handoff-2026-10-20`, based on upstream `main` at `b7bb635`. The authenticated connector account and local Git account have no upstream push permission. A standard fork under the authenticated `mati4193` account was prepared for the pull request; upstream history and Pages configuration are unchanged. No force-push, merge, AdMob submission or approval of final policy text is part of this revision.

The published website predates this revision. Local validation does not establish deployment of these corrections. After review/merge and successful Pages deployment, check the exact public URL and in-game link on Android and signed out. The external web-reading tool could not fetch the existing public policy during this session; that failure is not evidence of an HTTP 404 or deployment failure.

## App and approval limits

No Android device, final AAB, mailbox, AdMob account or Play Console was tested here. The engineering handoff reports source and validation-artifact findings; it does not prove all SDK traffic or provider retention/deletion. Remaining audience/territory, age handling, support/rights/retention/legal decisions, final-candidate matching and Android consent/network/reward/notification/backup tests are recorded in [PRIVACY_REVIEW.md](PRIVACY_REVIEW.md).

**Ready for review of these corrections; not ready for final policy approval or AdMob submission.**
