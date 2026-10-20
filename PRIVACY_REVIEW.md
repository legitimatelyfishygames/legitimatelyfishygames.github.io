# Privacy review — Kitchen Chaos: Idle Cooking

Reviewed: **19 October 2026**. Status: **DRAFT — awaiting the final game handoff; not approved as the final Google Play or AdMob privacy policy.** No effective date is set.

Intended policy URL: `https://legitimatelyfishygames.github.io/games/kitchen-chaos/privacy.html`.

## Confirmed context and evidence limits

- Developer/studio display name: **Legitimately Fishy Games**.
- Public privacy/support contact: **mati4193.004@gmail.com**. The HTML policy now includes a working `mailto:` link. The address is no longer a missing factual input; inbox monitoring and retention still need operational review.
- Platform: Android through Google Play. Status: under development, preparing for the first closed test. No public release date or valid Play download destination has been supplied.
- The user-provided pre-integration audit identified local JSON saves, progression, manager inventory, random-box state, currency state, settings, app-created save backups and migration copies, and optional local quest notifications.
- That audit detected no developer-operated player account/cloud-save server and no real Google Play Billing implementation. These are scoped audit findings, not assurances about every dependency or the final build.
- An **older APK contained Unity LevelPlay / Unity Ads advertising dependencies**. A separate game project is replacing them with direct AdMob and UMP. Neither removal nor final native SDK processing has yet been established by the website's evidence.
- `PRIVACY_HANDOFF_WEBSITE.md` is the required factual handoff from the Unity work. It has not been supplied for review in this update. Use it as the main app-specific input when it arrives, and reconcile it with the final build evidence. Generic SDK documentation does not prove the actual app configuration.

The site can technically serve a draft, but an accessible URL and a valid email do not resolve the final policy's factual blockers.

## Release milestones — keep separate

| Milestone | Supplied intended scope | Policy treatment |
| --- | --- | --- |
| First closed test | Core idle gameplay, local saves/offline progression, managers, random manager boxes obtained with earned in-game currency, optional AdMob rewarded ads, UMP, optional local notifications | Primary scope of the current draft. Verify against the actual test artifact before approval. Real-money purchases are not required for this milestone. |
| Future production | Google Play Billing diamond packs; purchased diamonds usable for random manager boxes; purchase processing, verification and recovery; applicable odds disclosures | A future plan. No real Billing integration was detected in the supplied audit. Do not describe payments as implemented in the closed test. Review and update policy and other disclosures before introducing paid features. |

## Closed-test publication blockers

- [ ] Receive and review `PRIVACY_HANDOFF_WEBSITE.md` for the exact closed-test release candidate. Identify what was tested, what remains inferred and what has not been tested.
- [ ] Verify all advertising/native dependencies in the final APK/AAB, including whether legacy LevelPlay/Unity Ads components and initialization paths remain. Do not say they have been removed based only on source edits or an old package list.
- [ ] Establish final SDK data processing with version-matched provider disclosures, effective configuration and runtime/network evidence. There is no basis for “the app collects no personal information.”
- [ ] Verify UMP messages, ad-request gating and the actual privacy options/withdrawal UI where required. Add exact user-facing steps only after implementation and device testing.
- [ ] Decide the actual audience and release countries, with child/teen age handling and any required parental/advertising treatment. A proposed 13+ audience does not resolve every country's child privacy or age-of-consent requirements.
- [ ] Verify app-created saves, backups/migration copies and reset/deletion behavior, plus the final Android backup/device-transfer rules. Do not claim New Game or uninstall removes every copy.
- [ ] Confirm the notification package, optionality, relevant permissions, stored scheduling data and disable/cancel behavior.
- [ ] Finalize studio-held information retention criteria, rights-request handling, security, international processing, applicable legal grounds and legally required developer identity/location details. Do not invent a company registration or physical address.
- [ ] Reconcile final policy, Play Data safety, ads/audience declarations, app controls and AdMob configuration. Approve the finished policy and set its effective date only after these facts are established.

## Required handoff from the Unity project

Ask the game project to include the following in `PRIVACY_HANDOFF_WEBSITE.md`. Label each statement as verified in the named artifact, source-only evidence, intended behavior or unresolved.

### 1. Build identity and dependency evidence

- [ ] Provide package/application ID, version name/code, build timestamp, Unity version, release-candidate filename and an artifact hash. State whether the evidence concerns an APK, AAB, exported Gradle project or source only.
- [ ] Supply the final Unity package/plugin inventory, resolved Gradle dependency tree and relevant native libraries/AARs/adapters. List direct and transitive Google, Unity, mediation, analytics, diagnostics, notification and engine-service components with versions.
- [ ] Show whether LevelPlay, Unity Ads and related adapters, manifests, initialization calls and native dependencies are absent or still present in the final artifact. If retained, document their role, data processing and provider disclosures; update the public provider list accordingly.
- [ ] Supply the final merged Android manifest and applicable generated resources, not just the project's source manifest. Record all permissions, exported components/services/providers and initialization behavior that may affect data flows.
- [ ] Identify standalone analytics, crash reporting, remote configuration, online accounts, cloud saves, Play Games or other online services if any. If the answer is “not found,” state the inspection coverage rather than converting it into an unqualified guarantee.

### 2. Local data, backup and deletion

- [ ] List every save/settings file, preference store, cache, app-created backup and migration copy, with its location and data fields. Identify manager inventory, random-box state, currency state, progression/offline timestamps and identifiers without assuming the list is exhaustive.
- [ ] Explain why each category is retained, when backup/migration copies are created or replaced, and what happens to old versions. Confirm whether any files are uploaded, exported, shared or accessible outside app storage.
- [ ] Document final `android:allowBackup`, `android:fullBackupContent` and `android:dataExtractionRules` values and the effective inclusion/exclusion rules for the supported Android versions. Review cloud backup and device transfer separately; a manifest flag alone may not settle every manufacturer's transfer behavior.
- [ ] Test New Game/reset against the primary save, preferences, backup files and migration copies. State exactly which files remain or can restore progress. Do not advertise New Game as complete deletion without evidence.
- [ ] Test Android clear-storage, uninstall/reinstall and backup/restore/device-transfer scenarios on relevant devices. Record limitations and any retained/restored data. Distinguish app-created local backup copies from Android-managed backup datasets.
- [ ] Provide accurate user instructions for deleting local data once verified. State what the studio can and cannot access or erase remotely and how provider-held information is handled.

### 3. Ads, UMP and runtime processing

- [ ] Identify the actual AdMob Unity plugin, native Android Mobile Ads SDK and UMP versions, ad formats, optional features and any mediation/bidding partners. Match official data disclosures to those installed versions.
- [ ] Document the final ad-request configuration: identifier handling, applicable non-personalized/limited modes, child-directed and under-age-of-consent treatment, content settings and regional messages. Do not assume declining personalization prevents all processing.
- [ ] Explain rewarded-ad behavior, including when SDKs initialize or send requests before a player chooses an ad, what eligibility gates requests and whether a server-side verification/user/custom identifier is sent.
- [ ] Provide the actual privacy options control text, location, availability conditions and steps for revisiting choices where required. Describe what changes take effect and when. Do not infer an implemented control from UMP's capabilities.
- [ ] Test fresh install, each available consent decision, later changes, expired decisions, error/offline behavior and relevant regions. Check initializations and requests as well as visible ad presentation. Record development debug settings separately from release behavior.
- [ ] Include scoped runtime/network evidence for cold start, consent not yet completed, applicable refusal/opt-out, an ad request/view, settings changes and notifications. Identify contacted domains/providers and the data categories supported by evidence; mark encrypted or unobserved processing as unresolved.
- [ ] Confirm test-ad/test-device settings appropriate to development and closed testing, and verify that development-only UMP forced geography/reset behavior is not accidentally used as the real production flow. Test ads are not proof of zero personal-data processing.

### 4. Optional notifications

- [ ] Name the notification plugin/native components and versions. Confirm whether reminders are entirely scheduled locally and whether any push tokens, remote service, analytics or network component is present.
- [ ] List scheduling fields, identifiers, timestamps, stored preferences and cancellation rules. State whether these remain after disabling notifications, reset or reinstall.
- [ ] Provide the actual opt-in/opt-out controls and supported Android permission behavior. Test permission refusal, permission revocation, in-game disable, cancellation of already scheduled notifications and reset behavior. Do not publish unimplemented tap instructions.

### 5. Closed-test declarations and audience

- [ ] Confirm that no real-money purchase processing is active in the named closed-test build. Record any dormant billing dependencies or test code separately from an implemented purchase feature.
- [ ] Supply final target age groups, regions and the rationale for any age handling. Confirm appropriate treatment of children, teenagers and users of unknown age, rather than treating 13 as a universal legal threshold.
- [ ] Supply proposed Play Data safety answers with the evidence behind each collected/shared category, purpose and deletion/security answer. Include SDK processing even when the developer cannot access individual records.
- [ ] Align ads, target-audience, content-rating, tester-facing disclosures, policy links and AdMob messages with the same final artifact. Determine any required random-box/odds disclosures for the closed-test configuration itself.

### 6. Remaining studio decisions

- [ ] Confirm any legally required identity/location disclosures behind the supplied studio display name. Do not invent business details.
- [ ] Confirm the supplied Gmail inbox is monitored for support/privacy requests. Establish proportionate identity checks, applicable deadlines, escalation/provider coordination and a clear response process.
- [ ] Set documented retention periods or justified criteria for support emails, attachments, reports and any other studio-held information, including backups. State when information may need retaining for legal or dispute purposes; do not invent fixed durations.
- [ ] Identify developer/provider locations, release regions, international transfer arrangements and relevant safeguards/disclosures. Verify applicable legal grounds, rights and complaint routes. Do not copy a provider's legal grounds as the studio's own assessment.
- [ ] Verify actual storage and transmission protections without claiming all data is encrypted or that security is absolute. Distinguish local game files from SDK traffic and Gmail handling.

## Future production — separate review before paid features

These items do not require describing future purchases as present in the closed test. They become necessary before the paid production scope is introduced.

- [ ] Confirm implementation and exact Google Play Billing versions, product types and purchase flow for diamond packs; document purchase data, transaction/purchase identifiers, tokens and recipients.
- [ ] Identify purchase verification infrastructure, ownership checks, acknowledgement/consumption, recovery, refund/revocation handling and retention. Do not promise server-side verification or restoration until implemented and tested.
- [ ] Explain how earned and purchased currencies are distinguished and how purchased diamonds interact with random manager boxes. Assess applicable regional paid-random-reward requirements, age protections, content/rating declarations and odds disclosures using the actual implementation.
- [ ] Update privacy policy, Play Data safety and purchase/consumer disclosures for the actual new processing before enabling payments. Add provider details and deletion/retention rules for verification or other services if introduced.
- [ ] Reassess audience, geographic availability, purchase controls and applicable legal requirements for paid random boxes. The future plan alone is not an implemented, approved or universally permitted purchase model.

## Website and final policy sign-off

- [ ] Keep the studio website free of studio-added analytics, advertising scripts, tracking cookies and unnecessary external embeds. Hosting/browser processing and voluntarily sent email are separate and are described in the policy.
- [ ] Verify the actual GitHub Pages host and retain its hosting-level IP security-log disclosure. Do not replace “no studio tracking scripts” with “no visitor data is processed.”
- [ ] Confirm the public Gmail link works and that published contact details match Play and the studio's support arrangements. Test locally without sending a message automatically.
- [ ] Resolve the draft's app-specific qualifications using the handoff, with remaining uncertainty reported rather than hidden. Review the final wording; remove the draft warning and set an effective date only when approved for publication.
- [ ] Verify the deployed policy over HTTPS in an ordinary mobile browser, without login, downloads, cookie acceptance or broken assets/navigation. Local testing is not deployment confirmation.
- [ ] Link the same approved policy from inside the game, Google Play Console and AdMob. A draft should not be presented as the finalized policy merely because its URL loads.
- [ ] Archive the approved text with the build/configuration it describes and establish review triggers for SDK, audience, data, purchase and provider changes. Define any required notice or renewed-consent process without promising a channel that does not exist.

## Official references rechecked

Checked on **19 October 2026**. These sources explain provider/platform behavior and inform the questions above; they do not prove what the final game contains.

- [Mobile Ads Unity data disclosure](https://developers.google.com/admob/unity/privacy/play-data-disclosure): documented SDK categories, purposes and developer responsibility for app-specific disclosures.
- [UMP Unity integration](https://developers.google.com/admob/unity/privacy): consent refresh, ad-request eligibility and conditional privacy options entry point.
- [Mobile Ads Unity test ads](https://developers.google.com/admob/unity/test-ads): development testing configuration.
- [Google's partner-app information](https://policies.google.com/technologies/partner-sites), [Google Privacy Policy](https://policies.google.com/privacy) and [Google retention information](https://policies.google.com/technologies/retention): Google processing, Gmail, transfers and provider-controlled retention.
- [Android Auto Backup](https://developer.android.com/identity/data/autobackup): app backup rules and device-transfer limitations.
- [Android notification permission](https://developer.android.com/develop/ui/compose/notifications/notification-permission): operating-system permission behavior, not proof of implemented game controls.
- [Google Play target audience guidance](https://support.google.com/googleplay/android-developer/answer/9867159): audience declarations and regional child/teen considerations.
- [ICO individual rights guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/individual-rights/individual-rights/): a regional reference, not a finding that the developer is established in the UK.
- [GitHub Pages data collection](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection) and [GitHub Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement): hosting-level processing.
