# Authentication

All API calls require authentication.
Authentication with the API is done using a HTTP header.

Your S2 Partner account manager will set these up and communicate them with you. 

You will have two access keys, one for the test environment and the other for the production environment.

- X-AccessKey: Your access key

```sh
curl -X 'GET' \
  'https://s2-api.ventmere.io/partner/fulfillment' \
  -H 'accept: application/json' \
  -H 'X-AccessKey: YOUR-ACCESS-KEY (DEV)'
```

```sh
curl -X 'GET' \
  'https://api.s2sell.com/core/partner/fulfillment' \
  -H 'accept: application/json' \
  -H 'X-AccessKey: YOUR-ACCESS-KEY (PROD)'
```

Your API access key carries many privileges, so be sure to keep them secure! Do not share your secret API access keys in publicly accessible areas such as GitHub, client-side code, and etc.


All API requests must be made over HTTPS. API requests without authentication will also fail.