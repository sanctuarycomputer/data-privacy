# Data Privacy & You
![](https://media.giphy.com/media/3o7TKEdVH8csXxKDO8/giphy.gif)

Data privacy, accountability, and security are becoming central concerns for web and app developers. This living document provides a series of resources to help us design and maintain our sites' compliance with the [GDPR](https://www.eugdpr.org/).

## What is the GDPR?
Simply put by [ZDNet](https://www.zdnet.com/article/gdpr-an-executive-guide-to-what-you-need-to-know/):

>At its core, GDPR is a new set of rules designed to give EU citizens more control over their personal data. It aims to simplify the regulatory environment for business so both citizens and businesses in the European Union can fully benefit from the digital economy.
>The reforms are designed to reflect the world we're living in now, and brings laws and obligations - including those around personal data, privacy and consent - across Europe up to speed for the internet-connected age.

### What does this mean?
This means organizations are now in charge of their own compliance with these regulations. All aspects of their data-related ecosystem must be fully compliant or they face fines up to 4% of their annual earnings or €20 million – whichever is larger. Obviously, this isn't a penalty that business owners can brush off. Business-owners and data-managers are now forced to be proactice, not reactive, on the subjects of data policy, security, and transparency.

### Why does this matter?
_"I'm in America, and so are my clients. Why does this matter to me?"_ This is a common reaction. But chances are there's someone in the EU that uses your site (even if they only visited once on an EU-located WiFi network). This automatically makes this regulation apply to you. Whether your app services the EU or not, you could be putting EU citizens at risk.

In addition to this, the US will soon follow up with their own version of this policy. While it is predicted to be lightweight in requirement, it doesn't hurt to meet this stricter set of compliance to ensure everyone is happy.

## What needs to be done?

### Add a Privacy Policy
Contrary to popular practice, privacy policies are not for the service provider's benefit – it's for the service users' benefit. This means the privacy policy should be written with _them_ in mind. Use the following tips when crafting a privacy policy:

- Make sure your Privacy Policy is written to be read – not to absolve you of any fault or liability in a court of law.  If your Privacy Policy is not _plain-English enough_, it may void your entire policy, leaving you vulnerable to maximum penalties. This means no all-caps paragraph blocks of sans-serif font. No rare, 17th-century words that nobody uses. No massive 3-paragraph-long sentences without any punctuation. Use conversational English. Use short, straight-forward sentence structure. Use section titles and list elements when needed. This should be a friendly, yet succinct document.

- Make sure your Privacy Policy appoints a Data Privacy Officer / Data Protection Officer by name and list contact information for this person. This can be as simple as appointing the tech lead of a project and allowing them to be contacted through privacy@example.com.

- Make sure your Privacy Policy lists what user data is collected and when it is collected.

- Make sure your Privacy Policy lists how user data is used, when it is used that way.

- Make sure to include a brief description as to why your app collects certain points of data. Every datapoint collected is required to have a business-critical, easily justified reason it's collected. You can't collect user data that won't ever be used by your app. It's okay to collect additional, non-app related information for the sake of _selling user data_, you just have to plainly say that's why those datapoints are collected (this leaves you open to other infractions, but you get the picture).

- Make sure your Privacy Policy acknowledges a data subject's (users) rights and how they can go about using them to make data requests. This can be as simple as asking them to email privacy@example.com to make any requests.

After this document is successfully written and uploaded, you must clearly link to it on your site. This means it (or a link to it) is present at every data-entry point: checkouts, sign-up forms, newsletter opt-ins, invite-a-friend inputs.

### Guarantee your app enables GDPR's Article 15 (Data Subject's Rights)
Among the [individual rights that users now have](https://ec.europa.eu/info/law/law-topic/data-protection/reform/rights-citizens_en) are the rights to access personal data, erasure, rectification, and portability. As a developer, you might be able to see the parallels between these rights and CRUD operations. Simple put, users have the right to: 

- ask for a list of all datapoints that are associated with their identity within your app
- ask to delete all of their identity-associated information within your app
- ask to add or edit any of their identity-associated datapoints for the sake of correction
- ask for a copy of their identity-associated data

You have a month to fulfill these requests. This means you have to make sure your app can easily fulfill any one of these request types within the scale it operates – and do it without breaking things. If a user wants their information to be deleted, you must. Make sure your app and any dependent analytics services have a way to securely and safely anonymize information.

### Meet security and transparency baselines
As a scurity baseline, we should be installing and forcing SSL on all properties. Even for our blogs and portfolios. [Let's Encrypt](https://letsencrypt.org/) offers free SSL and programmatic SSL generation, so there's no excuse. [Bcrypt](https://en.wikipedia.org/wiki/Bcrypt) is the defacto encryption method when hashing sensitive data.

If there is any instance of leak, breach, or security mishap it must be reported immediately:

>Personal data breaches should be reported within 72 hours to the local authority. You should report what data has been lost, what the consequences are and what countermeasures you have taken. Unless the data leaked was encrypted, you should also report the breach to the person (data subject) whose data you lost.

Failure to do so leaves you liable to the full extent of GDPR penalties and other public endangerment laws depending on your business's and your data subject's locales.

## Resources

- [Official EU GDPR Resources](https://ec.europa.eu/commission/priorities/justice-and-fundamental-rights/data-protection/2018-reform-eu-data-protection-rules_en): Multi-lingual guides to explain the GDPR direct from the EU
- [Shopify GDPR Whitepaper](https://help.shopify.com/assets/pdfs/gdpr-whitepaper.pdf): Great explanation of the GDPR and how Shopify and Shopify sites are examples of _Data Processors and Controllers_
- [MailChimp's GDPR Whitepaper](https://kb.mailchimp.com/binaries/content/assets/mailchimpkb/us/en/pdfs/mailchimp_gdpr_sept2017.pdf): Another good example of a large, familiar service provider applying the GDPR to themselves
- [GDPR Checklist](https://gdprchecklist.io/): Robust checklist of items to consider when achieving compliance
