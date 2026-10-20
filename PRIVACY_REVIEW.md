# Privacy review — Kitchen Chaos: Idle Cooking

Reviewed: **20 October 2026**. **DRAFT — engineering handoff reconciled; final candidate, device testing and developer decisions outstanding. Not approved for final Google Play or AdMob submission.** No effective date is set.

Policy URL: <https://legitimatelyfishygames.github.io/games/kitchen-chaos/privacy.html>. The website is published through GitHub Pages. These corrections require review, merge and deployment. The handoff's earlier 404 observation is historical, not a finding about the updated deployment.

## Primary technical evidence and limits

The complete **PRIVACY_HANDOFF_WEBSITE.md**, prepared 19–20 October 2026 in the Unity project, is the primary app-specific source, supplied from `KitchenChaosIdleFactory/PRIVACY_HANDOFF_WEBSITE.md`. It supersedes the older paid-launch/pre-integration audit for this closed test. Its statements are engineering evidence, not legal approval or authorization for unrelated website actions.

The handoff reports source inspection plus manifest/dependency and derived-APK DEX inspection of a new non-development **validation AAB**. We reviewed the handoff, not the underlying artifact or its separate `CLOSED_TEST_IMPLEMENTATION.md` report. Do not assume the validation AAB is the final candidate. Source/controller tests and packaging inspection do not prove live SDK processing, every network path, phone consent behavior or production account configuration.

## Resolved findings from the handoff

These are recorded findings, not outstanding requests to repeat the old audit:

| Topic | Finding and evidence scope |
| --- | --- |
| Identity | Legitimately Fishy Games; Kitchen Chaos: Idle Cooking; **mati4193.004@gmail.com**; intended package `com.legitimatelyfishygames.kitchenchaos`. Historical prototypes use `com.kitchenchaos.idlefactory.prototype` and separate data. No company registration/address inferred. |
| SDKs | Unity 6000.4.6f1; Google Mobile Ads Unity 11.6.0 with UMP Unity bridge; native GMA 25.5.0 and UMP 4.0.0 resolved/present in the reported validation artifact; Unity Mobile Notifications 2.4.3; External Dependency Manager 2.1.0 for Editor/build resolution. |
| Previous ad stack | LevelPlay 9.5.1, adapter and hook removed from source. Old ironSource/LevelPlay/Unity Ads packages, native dependencies and startup components absent in the reported validation artifact. Historical APKs retain them; this does not establish final-candidate absence. |
| Native support | Google ads-identifier 18.0.0, appset 16.0.1 and measurement support remain. Reported manifest includes Internet/network state, advertising ID, Ad Services ID/attribution/topics, Wake Lock/Foreground Service support, internal signature receiver permission and optional notifications. No Billing, GPS, camera, microphone, contacts or broad storage permission appears in that artifact. Permissions do not prove actual access/traffic. |
| Services | No extra mediation, standalone analytics/crash upload, developer account/cloud save/custom backend or remote push service introduced; no authored endpoint receives gameplay saves. Advertising measurement is separate from these scoped findings. |
| Consent code | Launch refreshes UMP, shows a required form and checks `CanRequestAds()` before initialization/request/show. Refusal is not unrestricted non-personalized-ad permission; partial choices and valid prior-session permission during errors remain SDK decisions. No game-owned consent cache replaces UMP. |
| Player controls | Options includes policy browser link and **Ad privacy choices**, visible/interactable when UMP requires it. Changes invalidate cached/in-flight ads. Implemented code; regional phone behavior remains untested. Reset/defaults do not erase provider records. |
| Rewards | Genuine client callback grants at most once to original saved destination; closing/failure/no-fill/offline grants none. No developer server-side verification endpoint; receipt IDs are not AdMob user IDs/custom verification data. Device behavior still needs testing. |
| Activation | Development Android and validation/test-inventory AABs use official rewarded test unit; desktop TEST AD is simulation. Ordinary production compilation selects owner's rewarded unit, but `audienceReviewed=false` blocks production advertising pending owner review/device validation. |
| Local persistence | Readable JSON stores progression, economy, managers, chest/pity/committed outcomes, claims and offline state; options separate. Local run/opening/ad-attempt IDs/reservations support idempotency. Throughput samples have no authored telemetry sender; notebook search text is transient with no authored persistence/upload found. |
| Backups/reset | Atomic validated replacement, recovery `.bak`, immutable migration `.before-...json`, timestamped New Game pre-reset copies. New Game retains options/backups; ascension retains permanent progression; Restore defaults changes settings. No comprehensive Delete local data or age/count pruning. No fixed retention or complete deletion promised. |
| Android backup | No explicit authored backup/transfer rules configured in this work. Eligible files/SDK preferences may be included under defaults/account/device conditions. Not developer cloud save or guaranteed recovery. |
| Security | Unkeyed SHA-256 is corruption checking, not encryption/protection against malicious edits. Every SDK transmission path has not been verified. |
| Notifications | Optional, **off by default**, local quest forecast/reminder. Enable requests permission; code cancels on disable/resume. Lock screen may show products/masked recipes. No FCM/push-token integration added; device behavior awaits testing. |
| Economy | Earned currencies and manager chests, including chests bought with earned diamonds. No real Billing, money charged or Play purchase tokens; release UI omits paid prices/checkout/test grants. TEST FREE packs are development tools. Paid diamond packs/purchased diamonds for random chests belong to future Milestone B. |

## Remaining developer decisions and operational/legal review

- [ ] Decide age groups and countries, including proposed ages 13–15, 16–17 and adults, and below-consent/unknown-age handling. No age screen, birth-date collection or verified-adult status exists. Development teen treatment/T content cap and UMP under-consent=false do not establish regional classification. Keep production gated until approved; determine needed code changes/parental protections.
- [ ] Review version-matched provider disclosures, final AdMob messages/account configuration, identifier settings and runtime evidence. Finalize Data safety categories, recipients, purposes, optionality, sharing exceptions and security/deletion answers. Optional ad viewing does not establish optional SDK processing; lack of developer access does not mean no personal data.
- [ ] Decide whether Android cloud-backup/device-transfer rules, bounded backup retention or comprehensive local deletion need implementing before this release. Record chosen scope and tested limits. These planned features are neither completed nor assumed mandatory for the closed test by this review.
- [ ] Confirm required developer identity/location disclosures, applicable legal grounds, regional rights/complaint routes, international processing and safeguards. Do not infer UK establishment from timezone or copy Google's legal basis as the studio's assessment.
- [ ] Confirm inbox monitoring/access, proportionate request checks, applicable response deadlines, provider referral/escalation and support-email/attachment retention criteria. Gmail/mailbox workflow was not inspected. Define what the developer can access/erase without promising provider-wide erasure.
- [ ] Review closed-test random-chest odds/contents, audience/territory and content-rating disclosures. Existing UI is not certified probability evidence or approval for paid random rewards.
- [ ] Reconcile policy, in-game controls/link, Play ads/audience/content-rating/Data safety declarations and AdMob configuration against the same approved candidate. Approve text, set effective date and establish change-review/notice process only after outstanding work is resolved.

## Remaining final-candidate evidence

- [ ] Identify actual closed-test candidate: package, version name/code, timestamp, filename and hash. Obtain implementation report, merged manifest and resolved dependency/code inventory; match SDK versions, legacy absence, permissions/startup components, backup rules and lack of Billing to that artifact. Do not substitute the validation AAB for this decision.
- [ ] Verify final build flags, audience guard, test/production inventory and absence of unintended debug geography/reset settings. Record approved closed-test inventory and criteria for any production activation.

## Remaining Android device checks

Use appropriate test inventory; record build identity, device/OS, region/test settings, results and evidence limits. Simulated/controller tests are not physical-device evidence.

- [ ] Test fresh/returning/expired consent, every offered choice, regions and offline/error paths including valid prior-session eligibility. Check initialization/request gating, conditional **Ad privacy choices**, reopening/changing choices and invalidating ads; verify policy browser link.
- [ ] Inspect scoped cold-start, pre-choice, refusal/opt-out, ad request/view and privacy-change traffic/identifier access. Record services and supported categories; leave encrypted payloads/unobserved paths uncertain. Do not claim all SDK flows or every transmission protection verified.
- [ ] Test real client reward callbacks, closing/failure/no-fill/offline and stale/in-flight ads against original saved transactions; verify at-most-once grants on device.
- [ ] Exercise New Game, ascension and Restore defaults against main/options/recovery/migration/pre-reset files. Test Clear storage, uninstall/reinstall, Android backup/restore and device transfer under relevant OS/account/device conditions before publishing deletion/recovery instructions.
- [ ] Test notifications initially off, opt-in, permission denial/revocation, reminder text/lock screen, disable/resume cancellation and reset/reinstall effects. Verify notification permission is independent of ad consent.
- [ ] After merge/deployment, test exact revised HTTPS policy signed out in an Android browser and via game Options: readable without login/cookie gate, correct draft, assets/navigation working. Local responsive checks do not prove on-phone behavior or revised deployment.

## Separate future payment milestone

Before activating paid diamond packs, review actual Billing flow/version, transaction IDs/tokens, verification, acknowledgement/consumption, durable fulfilment/recovery/refunds and retention; assess purchased diamonds for random chests, age/territory/purchase protections and odds/consumer disclosures; update policy/platform declarations. These are future activation gates, not claims that payments exist or requirements to implement payments in the closed test.

## Website validation and approval

The confirmed contact and appropriate Google links remain. Branding, CSS, JavaScript and site structure are preserved. The static site has no studio-added analytics, ad scripts, tracking widgets/cookies; hosting/browser connections and voluntary email remain separate processing. See [PRIVACY_VALIDATION.md](PRIVACY_VALIDATION.md) for checks and publication limits.

An accessible draft URL is not approval. **Not ready for final approval or AdMob submission** while the decisions, final-candidate review and Android checks above remain open.

## Official references

Rechecked **20 October 2026**: [Mobile Ads disclosure](https://developers.google.com/admob/unity/privacy/play-data-disclosure), [UMP Unity](https://developers.google.com/admob/unity/privacy), [Android Auto Backup](https://developer.android.com/identity/data/autobackup). These explain providers/platforms, not independent proof of game behavior. The Mobile Ads disclosure is maintained for the latest SDK; preserve version/configuration matching for final declarations.

Additional references: [test ads](https://developers.google.com/admob/unity/test-ads), [Google partner apps](https://policies.google.com/technologies/partner-sites), [Google privacy](https://policies.google.com/privacy), [Google retention](https://policies.google.com/technologies/retention), [notification permission](https://developer.android.com/develop/ui/compose/notifications/notification-permission), [Play audience](https://support.google.com/googleplay/android-developer/answer/9867159), [regional ICO rights](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/individual-rights/individual-rights/), [GitHub Pages data collection](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection), [GitHub privacy](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).
