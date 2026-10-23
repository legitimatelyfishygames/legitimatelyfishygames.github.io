# Kitchen Chaos closed-test privacy review and release checklist

Reviewed 23 October 2026 for **0.36.1 (43)**, package `com.legitimatelyfishygames.kitchenchaos`. Supersedes the 22 October active-AdMob/UMP description. Evidence: the owner's verified facts for the exact signed AAB; no independent game/build/network audit was performed here. No game repository, Unity files, AAB or Console settings were accessed or changed.

## Evidence and corrections

- Native Google Mobile Ads and UMP, advertising permissions and active ad/consent initialization paths are excluded; rewarded ads disabled. Old policy sections 1, 4–6 and the game page incorrectly described current ads and UMP controls.
- Google Play Billing **9** and **BILLING permission remain**, but checkout is disabled and **no purchase connection occurs**. The library is neither absent nor offering paid packs.
- Managed SDK code reads device/app properties locally. No active off-device transmission was identified in audited startup paths; **complete absence of traffic across the distributed build was not independently established**.
- Gameplay, local saves/progression remain functional; signed build passed real-device gameplay and save/recovery tests. This does not verify all privacy paths, backup behavior or deletion.
- Audience **18+**; test territories **United Kingdom, Poland, United States, New Zealand**. No player accounts or proprietary cloud saves.
- Existing website evidence for optional local notifications, recovery/migration/pre-reset copies, Reset Progress limits and possible Android backups is preserved, not independently re-audited. Support/privacy email: **mati4193.004@gmail.com**.

## Google Play Data safety implications

[Google's Data safety guidance](https://support.google.com/googleplay/android-developer/answer/10787469) requires the form for closed testing. The internal-only exemption does not apply. The form is package-wide: cover applicable behavior across versions/regions currently distributed on Play, not future commercial plans alone.

| Area | Current implication / remaining question |
| --- | --- |
| Local saves and SDK reads | Processing confined to the device is outside Google's collection definition. Verify that it remains local on all relevant paths; local reads alone do not establish off-device collection. |
| Ads/UMP excluded | Do not copy active AdMob collection or advertising purposes from earlier plans. Reconcile the ads declaration with this artifact and any other active artifacts. |
| Billing disconnected | BILLING permission/library inclusion alone does not establish purchase-history collection. Disabled checkout also does not prove all SDK processing is local. Verify exact Unity IAP version, services and other execution paths. |
| Remaining SDKs/engine | Check launch, resume, background, gameplay, notifications, errors and delayed initialization. Record actual destinations, fields, triggers, purposes and recipients, including identifiers, diagnostics, crash logs or IP-derived location if present. No unverified category is asserted as collected. |
| Collection vs sharing | Include SDK/library flows. Assess sharing exceptions individually; a service-provider exception does not automatically exempt collection. On-device transfer to another app can be sharing. |
| Platform/backups/support | Separate independent Android/Play processing from app/SDK flows. Assess actual backup rules and user-initiated email/browser actions under Google's scope/exceptions. Do not automatically classify website hosting/Gmail as in-app collection. |
| Purposes/optionality | Disabled ads/checkout do not establish optional SDK collection. Assess actual flows, purposes, required/optional and ephemeral processing individually. |
| Security/deletion | Do not attest all collected data is encrypted in transit without evidence for every applicable flow. Reset Progress is not complete deletion. No studio accounts exist; do not invent an account-deletion flow. Assess deletion requests for actual studio/provider-held data separately. |

**Pending before declaration submission:** whether the entire relevant distributed app collects or shares any reportable data. Startup-path evidence is insufficient to approve “No data collected” or “No data shared.” Do not invent collection to fill uncertainty either. Obtain whole-build evidence and retain the basis for final answers. No Console declarations were submitted here.

## Current publishing checklist

- [x] Review website policies against the owner-confirmed exact AAB and remove current-ad/UMP contradictions.
- [x] Separate current disabled features from future ads/purchases on policy, game page and homepage; preserve saves, backups, support, rights and provider limits.
- [x] Document Data safety implications, uncertainties and exact activation wording.
- [ ] Before game submission, resolve whole-build SDK/transmission questions and reconcile Data safety, ads, audience, territories, content rating and permissions with all applicable active artifacts.
- [ ] Verify in-game policy link, notifications and reset controls on the distributed build. Gameplay/save tests do not substitute for privacy checks.
- [ ] Confirm Android backup/restore, transfer and deletion behavior before stronger promises.
- [ ] Each publishing cycle: compare policies against current features, SDKs/services, ads, analytics, purchases, permissions, data handling, accounts/deletion and audience. Reopen for new gaps; remind again if unresolved at submission.

## Advertising activation — exact wording to change

Before distributing a later ad-enabled build, update `games/kitchen-chaos/privacy.html`:

1. Section 1: replace “Rewarded advertisements and real-money checkout are disabled.” Split status if only one feature activates. Replace the following native-SDK/permissions/initialization exclusions with the actual new configuration.
2. Section 4: replace the paragraph starting “Current closed test — 0.36.1 (43)” and update the startup-audit paragraph to the new evidence. Replace “Planned later update” with verified SDK versions, data fields, recipients, purposes, controls and retention. [Google's SDK disclosure](https://developers.google.com/admob/unity/privacy/play-data-disclosure) is input, not proof of all configured flows.
3. Section 5: replace “Native Google advertising and UMP services are excluded from this closed-test AAB.” Reconcile providers and actual flows.
4. Section 6: replace “UMP consent is not operational in closed-test build 43” and the no-functioning-control statement. Turn future requirements into accurate current regional controls and tested menu instructions. Validate refusal, withdrawal/reopening, ad eligibility, error/offline paths and actual traffic using [UMP guidance](https://developers.google.com/admob/unity/privacy).
5. Update scope/version/effective date and section 15's future-update statement. Replace the game-page no-ads bullet and homepage disabled/excluded copy; move only activated features out of the planned milestone.
6. Reconcile Data safety, ads declarations, regional notices and consent configuration before distribution. Optional ad viewing does not establish optional SDK processing.

## Purchase activation — exact wording to change

1. Policy sections 1 and 5: replace disabled-checkout/no-connection statements with true status and flows; retain disabled-ad status if appropriate.
2. Section 13: replace the paragraph starting “Current purchase status — 0.36.1 (43), 23 October 2026”. Replace “Planned later update” with verified transaction processing: product IDs, order/transaction IDs, tokens/receipts, status, recipients, purposes, retention and fulfilment. Test pending/failure/refund and duplicate handling; do not promise consumable recovery without evidence.
3. Update scope/version/date, section 15, homepage and both game-page milestones. Retained Billing does not prove active transaction processing.
4. Verify installed Unity IAP version and enabled services against [Unity privacy guidance](https://docs.unity.com/en-us/iap/privacy-and-consent). Billing 9 is not the Unity IAP package version.
5. Verify actual random-manager odds and disclose them before and close to relevant paid purchases, including diamond packs. A policy sentence does not replace in-game disclosure. See [Play payments policy](https://support.google.com/googleplay/android-developer/answer/9858738).
6. Reconcile Data safety and regional consumer/random-reward requirements before activation.

## Remaining privacy operations questions

- Confirm required controller legal identity/location, establishment, legal grounds and any regional representative requirements. Studio display name is not evidence of registration.
- Define support-email/attachment retention and operate monitored request intake, verification, response deadlines, deletion and provider coordination. No fixed period or tested deletion process is invented here.
- Confirm transfer arrangements/safeguards for studio-controlled processing. Provider links are not a studio-specific legal assessment.
- Recheck duties for all four territories. An 18+ target is not age verification or a complete regional assessment.

Publishing factual website corrections does not resolve these declaration or operational questions.
