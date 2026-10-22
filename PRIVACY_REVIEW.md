# Kitchen Chaos privacy review and release checklist

Updated: **22 October 2026**. The public policy is finalized for publication on the owner's instructions. This is a website/policy review, not legal approval, an Android build audit or certification of Play Console declarations.

## Evidence and resolved corrections

The owner confirmed the following on 22 October 2026, superseding conflicting 19–20 October draft/handoff statements:

- Google Play target audience: **18+ only**. No teenage audience or worldwide availability is inferred.
- Current closed-test targets: **UK, Poland, US, New Zealand**; final public-release territories remain undecided.
- **AdMob rewarded ads and Google UMP are integrated**, including applicable user privacy choices.
- **Google Play Billing / Unity IAP is integrated for six diamond packs**. Real-money checkout is disabled pending product configuration and testing. It is incorrect to say Billing is absent.
- Diamonds can buy random manager chests. Purchased diamonds can do so when payments are enabled; reward odds must be disclosed before relevant paid purchases.
- Saves are local; **Reset Progress** exists. There is no player account system or proprietary cloud-save service. No complete deletion of backups/provider records is promised.
- Public contact: **mati4193.004@gmail.com**.

The existing website/earlier handoff supports local recovery/migration/pre-reset copies, optional local notifications, and Options → Ad privacy choices when UMP requires it. No current game files, AAB, device, Play Console, AdMob account or mailbox were inspected in this task. SDK-version and runtime claims in the old draft were removed rather than presented as final-build evidence. No game project was modified.

## Official documentation checked

- [AdMob Unity disclosure](https://developers.google.com/admob/unity/privacy/play-data-disclosure) and [Android disclosure](https://developers.google.com/admob/android/privacy/play-data-disclosure): SDK collection/sharing includes IP-derived general location, interactions, diagnostics and device/account IDs for advertising, analytics and fraud prevention. The Android page currently identifies version 25.5.0; version-match the distributed app.
- [UMP Unity](https://developers.google.com/admob/unity/privacy): refresh consent, show applicable forms, check ad eligibility and provide privacy options when required. Optional viewing does not establish optional SDK data collection.
- [Google Play data use](https://business.safety.google/privacy/google-services/play/): platform processing can include crash reports. This supports a separate crash-log disclosure, not attributing every crash to AdMob.
- [Unity IAP privacy](https://docs.unity.com/en-us/iap/privacy-and-consent): data handling changes by package version. Unity distinguishes versions before 5.4 from 5.4+ and enabled services. Do not infer no collection from disabled checkout or copy D2C/webshop behavior into a native-store-only integration.
- [Google Play Data safety](https://support.google.com/googleplay/android-developer/answer/10787469): include third-party SDK flows and distinguish local-only data, actual off-device collection, sharing exceptions and optionality.
- [Google Play payments](https://support.google.com/googleplay/android-developer/answer/9858738): disclose randomized-item odds before and close to the relevant purchase.

## Release checklist and unresolved factual questions

- [x] Review the existing public website policy against owner-confirmed current features; replace outdated audience, billing and reset statements and use the confirmed contact.
- [x] Keep current testing territories separate from the future release footprint.
- [x] Describe interactions, diagnostics, identifiers, approximate location and possible crash logs without promising no collection or global deletion.
- [ ] **Each publishing cycle:** compare the game, SDKs/services, ads, purchases, permissions, data collection/sharing/retention, accounts/deletion and intended audience against current website policies; resolve any new gaps before submission.
- [ ] Match the distributed AAB's actual SDK versions, permissions, initialization and enabled services to policy and Data safety declarations. In particular, confirm **Unity IAP version**, native-store/D2C configuration and any initialization-time IDs, device/session/country data or analytics connections. If additional flows exist, update the public disclosure before that build is distributed. The current conditional IAP paragraph is not a verified inventory.
- [ ] Identify the actual crash-log path and SDK/platform, whether it runs automatically or depends on user settings, recipients, purposes, sharing and retention. Do not add Crashlytics or another crash service to the policy without evidence.
- [ ] Test UMP in UK/EEA and applicable US configurations, refusal/partial choices, reopening choices, offline/error paths, and actual ad/identifier traffic. Do not assume every player is age-verified because Play targets 18+.
- [ ] Confirm Reset Progress's current effects on main save, settings, backups and purchase/claim ledgers; test Android Clear storage, reinstall, backup/restore and transfer before making stronger deletion/recovery claims.
- [ ] Confirm notifications, public policy link and privacy controls on Android.
- [ ] Reconcile actual Play Console Data safety collection/sharing, purposes, optionality, encryption/deletion answers, audience, ads, content rating and territories with the same build. No Console declarations were edited here.

## Purchase activation — exact wording to change

- [ ] Configure and test all six products, charge/fulfilment/failure/pending/refund paths and duplicate prevention. Verify which product IDs, receipts/tokens/order IDs and statuses reach the game, Google, Unity or any other recipient, and their retention. Do not promise recovery of consumable diamonds without evidence.
- [ ] Validate reward odds and make disclosures clearly visible before and close to the paid purchase leading to random manager rewards, including diamond-pack purchases. A privacy-policy sentence alone does not satisfy this. Review territory-specific consumer/random-reward rules.
- [ ] **Replace section 13's paragraph beginning “Current purchase status (22 October 2026)”** with the true activation status. Remove the instruction to update that wording from section 15 once done; update the effective/updated date.
- [ ] Verify the “When purchases are enabled” transaction paragraph against the implemented flow and adjust any fields/recipients. Update website game/home payment-status copy and Data safety answers at the same time.

## Unresolved legal and operational questions

- [ ] Confirm the controller's required legal identity/contact-location disclosures, establishment, legal grounds for each purpose and any regional representative requirements; the studio name is not evidence of company registration.
- [ ] Confirm applicable international-transfer arrangements and safeguards for studio-controlled processing. Provider privacy-policy links are not a studio-specific legal assessment.
- [ ] Define and operate support-mail/attachment retention criteria, inbox monitoring and privacy-request verification, response deadlines and provider coordination. The policy provides a contact and scope limits; it does not invent a fixed period or verified deletion workflow.
- [ ] Confirm applicable regional privacy/advertising and random-reward obligations for the selected territories before submission/activation. An 18+ target does not resolve all such obligations.

Publishing the requested factual policy does not resolve these questions. Further evidence may require a policy change before game submission or paid-purchase activation.
