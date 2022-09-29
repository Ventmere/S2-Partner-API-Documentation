# Fulfillment
---

## API: Get Fulfillments

[Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/query_fulfillments)

* **URL:**

    `/partner/fulfillment`

* **Method:**

    `GET`

* **URL Params**

| Parameter | Required | Description |
| ------ | ------ | ----- |
| `id_list` | No | List of fulfillment id |
| `next_token` | No | A token for use in pagination. Your subsequent call can include `next_token=xxxxx` in order to fetch the next page of the list |


## API: Create Fulfillment

[Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/create_fulfillment)


* **URL:**

    `/partner/fulfillment`

* **Method:**

    `POST`