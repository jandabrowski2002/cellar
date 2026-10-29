---
layout: doc
lang: en
title: Cellar Privacy Policy
effective: 20 October 2026
description: What data the Cellar app collects, why, and how long it keeps it.
alt: /prywatnosc
---

## §1. Data controller

1. The controller of the personal data of Cellar app Users is Jan Dąbrowski, ul. Kazimierza Wielkiego 41/8, 30-074 Kraków, Poland (the “Controller”).
2. For anything concerning personal data, write to [jandabrowski77@gmail.com](mailto:jandabrowski77@gmail.com).
3. The Controller has not appointed a data protection officer – it is not required to.
4. Capitalised terms (App, Account, Scan, Catalog, Cellar) have the meaning given in the [Cellar Terms of Service](terms).
5. This is a translation of the Polish [Polityka prywatności](../prywatnosc). In case of discrepancies, the Polish version prevails.

## §2. What data we process and why

The Controller processes only the data needed for the App to work. The legal bases are Article 6(1) GDPR: (b) performance of a contract, i.e. the Terms; (c) legal obligation; (f) the Controller's legitimate interest; and (a) consent.

| Data | Purpose | Basis | Retention |
| --- | --- | --- | --- |
| E-mail address, password (stored only by Firebase Authentication, as a hash, not in plain text), sign-in account identifier | Creating the Account, signing in, confirming the e-mail address, resetting the password | (b) | Until the Account is deleted |
| From a Google account: e-mail address, Google identifier, name, profile photo | Sign-in with Google, name and photo in the profile | (b) | Until the Account is deleted |
| From an Apple account: Apple identifier, e-mail address (including Apple's private relay address), name if the User shares it | Sign-in with Apple | (b) | Until the Account is deleted |
| Display name, own profile photo | User profile | (b) | Until changed or the Account is deleted |
| Cellar: bottles, statuses, quantity, ratings, notes, price, place of purchase | Keeping the Cellar, aggregate product rating in the Catalog | (b) | Until the entry or the Account is deleted |
| Scans: label photos, label text read on the phone, barcode, recognition result, date | Identifying the bottle | (b) | Scan history until the Account is deleted |
| As above | Daily limits, cost control, abuse protection | (f) | Until the Account is deleted |
| Label photos and text | Bottle thumbnails, improving label recognition | (f) | No fixed period; after the Account is deleted, without any link to the User |
| Information added to the Catalog and proposed changes | Shared Catalog | (b) and (f) | Catalog entry indefinitely; link to the Account until it is deleted |
| Plan, Premium expiry date, Account identifier in RevenueCat | Handling the Premium subscription | (b) | Until the Account is deleted |
| Payment events from RevenueCat (subscription type, store, country, price, transaction identifier) | Accounting and tax obligations | (c) and (f) | 5 years from the end of the tax year |
| Confirmations of rewarded ads watched (AdMob transaction identifier, date) | Granting extra Scans | (b) | Until the Account is deleted |
| IP address | Abuse protection (Scans-per-minute limit) | (f) | Only in server memory, a few minutes; not stored in the database |
| E-mail correspondence | Answering questions, complaints and reports | (b) and (f) | Until the matter is resolved, then until claims become time-barred |

Providing data is voluntary, but an Account cannot be created without an e-mail address (or a Google or Apple account). The Controller does not make decisions about Users based solely on automated processing that would have legal effects (Article 22 GDPR).

## §3. Scanning and artificial intelligence

1. Part of the recognition happens on the phone, without sending the photo to Google: reading the label text, reading the barcode and a preliminary check that the photo shows a label. This uses the Google ML Kit library, which may send Google anonymous diagnostic data about how it works.
2. The Controller's server receives the label photo (downscaled on the phone), the text read from it and the barcode. Before sending, the App removes metadata saved by the camera, including location, from the photo.
3. If the bottle cannot be identified by its barcode or text, the server sends the label photo or text to Anthropic's Claude model. Anthropic does not receive the User's e-mail address, name or Account identifier. Under Anthropic's commercial terms, this data is not used to train its models.
4. On the Premium Plan the model may search the internet for the bottle. The search engine receives only the text of the product query (e.g. the name and producer from the label).
5. Please photograph bottles and labels, not people, documents or other personal data.

## §4. Who we share data with

The Controller does not sell data. The App's server belongs to and is operated by the Controller. Data is shared only with companies without which the App could not work:

| Recipient | Data | Purpose | Role |
| --- | --- | --- | --- |
| Apple Distribution International (iCloud) | Backups of the data in §2 | Storing backups | Processor |
| Anthropic, PBC (USA) | Label photos and text | Identifying the bottle (§3) | Processor |
| RevenueCat, Inc. (USA) | Account identifier, Premium purchase data | Handling and verifying subscriptions | Processor |
| Google Ireland Ltd (Firebase Authentication) | E-mail address, password (as a hash), Google and Apple account identifiers, IP address and device data at sign-in | Sign-in, sending address confirmation and password reset e-mails | Processor |
| Google Ireland Ltd | Google account sign-in data | Sign-in with Google | Independent controller |
| Apple Distribution International | Apple account sign-in data | Sign-in with Apple | Independent controller |
| Google Ireland Ltd (AdMob) | Advertising identifier, device data, IP address, ad interactions | Showing ads on the Free Plan, confirming rewarded ads (§6) | Independent controller |
| Google (Google Fonts, ML Kit) | IP address, anonymous diagnostic data | Downloading the App's fonts, on-device label reading | Independent controller |
| Apple Distribution International, Google Commerce Ltd | Purchase and payment data | Selling Premium in the App Store and Google Play | Independent controller |

The Controller does not see card details or any other payment method – these are handled by the store. Data may also be disclosed to public authorities where required by law.

## §5. Transfers outside the European Economic Area

1. Anthropic and RevenueCat are based in the USA, and Google and Apple may also process data outside the EEA.
2. Transfers are based on the European Commission's adequacy decision (EU-US Data Privacy Framework) where the recipient is certified under it, or on standard contractual clauses approved by the Commission (Article 46(2)(c) GDPR).
3. A copy of the safeguards can be requested at [jandabrowski77@gmail.com](mailto:jandabrowski77@gmail.com).

## §6. Ads and consent

1. On the Free Plan the App shows Google AdMob ads. There are no ads on the Premium Plan.
2. Before the first ad, the App asks Users in the EEA, the UK and Switzerland for consent to personalised ads and the use of device identifiers (a Google message). The basis is consent (Article 6(1)(a) GDPR).
3. Without consent, the App shows non-personalised ads. Google still processes some data (e.g. IP address, approximate location) to show the ad and prevent fraud.
4. Consent can be changed or withdrawn in the App at any time: Settings → Ad privacy. Withdrawing consent does not affect the lawfulness of processing before it was withdrawn.
5. On iPhone the App does not ask for access to the advertising identifier (IDFA) and does not track the User across other apps. On Android the advertising identifier can be reset or deleted in the phone settings (Google → Ads).
6. The App shows only ads intended for adult audiences and does not run ads directed at children.
7. More on how Google processes data: [policies.google.com/technologies/partner-sites](https://policies.google.com/technologies/partner-sites).

## §7. Data on the phone and permissions

1. On the phone the App stores only:
   1. sign-in session data – stored by the Firebase Authentication library (in the Keychain on iPhone, in the App's storage on Android),
   2. the App's server address and simple settings, such as the language.
2. The App does not use cookies or analytics tools to track the User.
3. The App asks for permissions only when they are needed:
   1. **camera** – label photos, barcodes, profile photo,
   2. **photos (library)** – choosing a label photo or profile photo; the App sees only the photos the User selects.
4. Permissions can be revoked at any time in the phone settings. Without the camera, a barcode can be typed in manually and a photo chosen from the library.
5. The App does not access the phone's location, contacts or audio recordings.

## §8. Your rights

1. The User has the right to:
   1. access their data and receive a copy (Article 15 GDPR),
   2. rectification (Article 16),
   3. erasure (Article 17),
   4. restriction of processing (Article 18),
   5. portability of data processed on the basis of a contract or consent (Article 20),
   6. object to processing based on legitimate interest (Article 21),
   7. withdraw consent at any time (Article 7(3)).
2. The Account, together with the Cellar, ratings, Scan history, profile photo and the sign-in account in Firebase Authentication, can be deleted by the User: Settings → Delete account.
3. Label photos and Catalog information remain after the Account is deleted, without any link to the User ([Terms](terms), §3 and §5). If a photo contains personal data (e.g. a face or a document), the Controller will delete it on request.
4. Other requests should be sent to [jandabrowski77@gmail.com](mailto:jandabrowski77@gmail.com). The Controller replies within one month. In exceptional cases this may be extended by two further months, of which the Controller will inform the User. The Controller may ask for confirmation of identity, e.g. a message from the Account's e-mail address.
5. The User may lodge a complaint with the President of the Personal Data Protection Office (Prezes Urzędu Ochrony Danych Osobowych, ul. Stawki 2, 00-193 Warszawa, Poland, [uodo.gov.pl](https://uodo.gov.pl)) or with the supervisory authority in their country of residence if they believe their data is processed unlawfully.

## §9. Final provisions

1. The App is intended only for adults. The Controller does not knowingly collect data from persons under 18. Such a person's Account will be deleted once reported.
2. The Controller protects data by, among other things, an encrypted connection (HTTPS) between the App and the server, storing passwords only as a cryptographic hash in Firebase Authentication (the App's server does not know passwords), restricted server access and regular backups.
3. The Controller announces changes to this policy in the App. Significant changes, e.g. a new purpose of processing or a new data recipient, are announced in advance.
4. This policy is effective from 20 October 2026.
