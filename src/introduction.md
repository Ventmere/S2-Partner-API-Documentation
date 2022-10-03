# Getting Started with S2 Partner API

## API Reference

The S2 Partner API is organized around [REST](https://en.wikipedia.org/wiki/Representational_state_transfer). Our API has predictable resource-oriented URLs, and uses standard HTTP response codes, authentication, and verbs.

The S2 Partner API doesn't support bulk updates. You can work on only one object per request.
## Onboarding

To use the S2 Partner API, you must first have valid credentials.

Once you have been approved, your account manager will send you API keys, see: [Authentication](./authentication)

## Test Environment

You can use the S2 partner API in test mode with the test base API URL, which doesn't affect your live data.

The dev base API URL is : `https://s2-api.ventmere.io/partner`

## Going Live

Once testing is complete, you can switch to production API.

The production API URL is: `https://api.s2sell.com/core/partner`