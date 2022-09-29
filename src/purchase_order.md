# Purchase Order
---

## API: Get Purchase Order

[Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/query_purchase_orders)

* **URL:**

    `/partner/purchase-order`

* **Method:**

    `GET`

* **URL Params**

| Parameter | Required | Description |
| ------ | ------ | ----- |
| `id_list` | No | List of order id |
| `next_token` | No | A token for use in pagination. Your subsequent call can include `next_token=xxxxx` in order to fetch the next page of the list |


## API: Create Purchase Order

[Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/create_purchase_order)

* **URL:**

    `/partner/purchase-order`

* **Method:**

    `POST`