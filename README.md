# Zip

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Zip is a global Buy Now Pay Later (BNPL) and digital wallet platform that enables merchants to offer flexible consumer payment plans at checkout. Accepted at over 63,000 merchants worldwide, Zip operates across Australia, New Zealand, the United States, Canada, and the United Kingdom.

## APIs

This repository catalogs three Zip REST APIs:

**Zip Global Merchant API** — Online checkout, charges, capture, refunds, and tokenisation (AU subscription payments). Base URL: `https://sand.merchant-api.com` (sandbox). Authentication: Bearer token.

**Zip US Gateway API** — North American order authorization, capture, refund, void, and confirmation with HMAC-SHA256 signature authentication (`X-QP-Signature` header). Base URL: `https://gateway.us.zip.co`. Supports both synchronous and asynchronous (webhook) response modes.

**Zip NZ In-Store API** — Point-of-sale order management for New Zealand retail environments. Bearer token via OAuth client credentials. Base URL: `https://zip.co/nz/api`.

## Developer Resources

- Developer Portal: https://developers.zip.co
- US Documentation: https://docs.us.zip.co/docs/introduction
- API Reference: https://developers.zip.co/reference/api-docs
- Sandbox Guide: https://developers.zip.co/v2/docs/sandbox
- GitHub (SDKs): https://github.com/zipMoney
- Status Page: https://status.zip.co
- Help Center: https://help.zip.co

## Integration Options

- Custom REST API integration
- Virtual Card (no backend changes required)
- Ecommerce plugins: Shopify, WooCommerce, BigCommerce, Magento 2, Salesforce Commerce Cloud
- In-store / point-of-sale

## Pricing

API access is bundled with the merchant agreement at no separate charge. Transaction fees (Merchant Service Fee) are negotiated commercially and vary by region and volume. Contact Zip at https://zip.co/au/business/payments to begin onboarding.
