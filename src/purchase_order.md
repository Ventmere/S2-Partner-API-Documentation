# Purchase Order

A purchase order is a customer's request to purchase one or more products from a shop. You can create and retrieve orders using the Purchase Order resource.

---

## API: Get Purchase Order

Learn more : [Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/query_purchase_orders)

* **URL:**

    `/purchase-order`

* **Method:**

    `GET`

* **URL Params**

| Parameter | Required | Description |
| ------ | ------ | ----- |
| `id_list` | No | List of order id |
| `next_token` | No | A token for use in pagination. Your subsequent call can include `next_token=xxxxx` in order to fetch the next page of the list |

* **Data Params**

    `None`

* **Success Response**
    * **Code:** `200` <br />
      **Content:**
      ```json
      [
        {
            "items": [
            {
                "completion_date": "2022-09-30T20:56:21.588Z",
                "created_at": "2022-09-30T20:56:21.588Z",
                "eta": "2022-09-30T20:56:21.588Z",
                "from_supplier": {
                "id": 0,
                "name": "string"
                },
                "id": 0,
                "items": [
                {
                    "completed_quantity": 0,
                    "quantity": 0,
                    "sku": "string"
                }
                ],
                "remarks": "string",
                "status": "pending",
                "to_warehouse_id": "string",
                "updated_at": "2022-09-30T20:56:21.588Z"
            }
            ],
            "next_token": "string"
        }
      ]
      ```

* **Sample Call:**
    ```sh
        curl -X 'GET' \
            'https://s2-api.ventmere.io/partner/purchase-order' \
            -H 'accept: application/json' \
            -H 'X-AccessKey: xxxxxxxxxxxxx'
    ```


## API: Create Purchase Order

[Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/create_purchase_order)

* **URL:**

    `/purchase-order`

* **Method:**

    `POST`

* **URL Params:**

    `None`

* **Data Params**

    ```json
        {
            "eta": "2022-09-30T21:06:03.806Z",
            "from_supplier_id": 0,
            "items": [
                {
                "quantity": 0,
                "sku": "string"
                }
            ],
            "remarks": "string",
            "to_warehouse_id": "string"
        }
    ```

* **Success Response**

    * **Code:** `200` <br />
      **Content:**
      ```json
        {
            "completion_date": "2022-09-30T21:06:03.808Z",
            "created_at": "2022-09-30T21:06:03.808Z",
            "eta": "2022-09-30T21:06:03.808Z",
            "from_supplier": {
                "id": 0,
                "name": "string"
            },
            "id": 0,
            "items": [
                {
                "completed_quantity": 0,
                "quantity": 0,
                "sku": "string"
                }
            ],
            "remarks": "string",
            "status": "pending",
            "to_warehouse_id": "string",
            "updated_at": "2022-09-30T21:06:03.808Z"
        }
      ```

* **Sample Call:**
    ```sh
        curl -X 'POST' \
            'https://s2-api.ventmere.io/partner/purchase-order' \
            -H 'accept: application/json' \
            -H 'X-AccessKey: xxxxxxxxxxxxx' \
            -H 'Content-Type: application/json' \
            -d '{
                "eta": "2022-09-30T21:10:19.904Z",
                "from_supplier_id": 0,
                "items": [
                    {
                    "quantity": 0,
                    "sku": "string"
                    }
                ],
                "remarks": "string",
                "to_warehouse_id": "string"
            }'
    ```