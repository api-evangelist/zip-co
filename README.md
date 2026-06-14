# Zip

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
