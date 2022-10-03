# Authentication

All API calls require authentication.
Authentication with the API is done using a HTTP header,

- X-AccessKey: Your access key

```sh
curl -X 'GET' \
  'https://s2-api.ventmere.io/partner/fulfillment' \
  -H 'accept: application/json' \
  -H 'X-AccessKey: YOUR-ACCESS-KEY'
```

Your S2 Partner account manager will set these up and communicate them with you.


Your API access key carries many privileges, so be sure to keep them secure! Do not share your secret API access keys in publicly accessible areas such as GitHub, client-side code, and etc.


All API requests must be made over HTTPS. API requests without authentication will also fail.