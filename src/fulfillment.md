# Fulfillment
You can use the `Fulfillment` resource to view fulfillments for a list of orders or a fulfillment order. A fulfillment represents work that is completed as part of a fulfillment order and can include one or more items. You can use the `Fulfillment` resource to manage fulfillments for both orders and fulfillment orders.

---

## API: Get Fulfillments
 
Learn more : [Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/query_fulfillments)

* **URL:**

    `/fulfillment`

* **Method:**

    `GET`

* **URL Params**

| Parameter | Required | Description |
| ------ | ------ | ----- |
| `id_list` | No | List of fulfillment id |
| `next_token` | No | A token for use in pagination. Your subsequent call can include `next_token=xxxxx` in order to fetch the next page of the list |

* **Data Params**

    `None`

* **Success Response**

    * **Code:** `200` <br />
      **Content:** 
      ```json
      {
        "items": [
            {
            "id": 120724,
            "fulfillment_warehouse_id": "system_84",
            "status": "shipped",
            "name": "Roland Ullrich",
            "address1": "85810 Sheridan Summit",
            "address2": "necessitatibus velit nisi",
            "address3": "incidunt aut culpa",
            "city": "Minnetonka",
            "province": "Rhode Island",
            "country_id": "AU",
            "zip": "93792",
            "phone": "(655) 941-4652 x31254",
            "items": [
                {
                "sku": "0zt9-5uk7",
                "quantity": 1
                }
            ],
            "shipments": [
                {
                "id": 119804,
                "status": "shipped",
                "carrier_id": "Australia Post",
                "tracking_numbers": [
                    "wn44vfhvqudkno3"
                ],
                "created_at": "2021-11-12T09:10:06.939357Z",
                "updated_at": "2022-08-23T17:26:32.815841Z",
                "items": [
                    {
                    "sku": "unknown_product_123899",
                    "quantity": 1
                    }
                ],
                "created_by": {
                    "id": 125,
                    "name": "Jerome Hoeger",
                    "email": "Jonatan.Connelly@hotmail.com"
                },
                "label_id": null,
                "label_type": null,
                "shipped_by": null,
                "remarks": "shawl"
                }
            ],
            "shipping_method": "standard",
            "warehouse_remarks": null,
            "created_at": "2021-11-11T11:56:04.568984Z",
            "updated_at": "2022-08-23T17:20:47.081115Z"
            }
        ]
      }
      ```

* **Sample Call:**
    ```sh
        curl -X 'GET' \
            'https://s2-api.ventmere.io/partner/fulfillment' \
            -H 'accept: application/json' \
            -H 'X-AccessKey: xxxxxxxxxxxxx'
    ```

## API: Create Fulfillment

Learn more : [Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/create_fulfillment)


* **URL:**

    `/fulfillment`

* **Method:**

    `POST`

* **URL Params**

    `None`

* **Data Paramss**

    ```json
        {
            "address1": "string",
            "address2": "string",
            "address3": "string",
            "city": "string",
            "country_id": "string",
            "fulfillment_warehouse_id": "string",
            "items": [
                {
                "quantity": 0,
                "sku": "string"
                }
            ],
            "name": "string",
            "phone": "string",
            "province": "string",
            "shipping_method": "standard",
            "zip": "string"
        }
    ```

* **Success Response**

    * **Code:** `200` <br />
      **Content:** 
      ```json
        {
            "address1": "string",
            "address2": "string",
            "address3": "string",
            "city": "string",
            "country_id": "string",
            "created_at": "2022-09-30T19:39:56.848Z",
            "fulfillment_warehouse_id": "string",
            "id": 0,
            "items": [
                {
                "quantity": 0,
                "sku": "string"
                }
            ],
            "name": "string",
            "phone": "string",
            "province": "string",
            "shipments": [
                {
                "carrier_id": "string",
                "created_at": "2022-09-30T19:39:56.848Z",
                "created_by": {
                    "email": "string",
                    "id": 0,
                    "name": "string"
                },
                "id": 0,
                "items": [
                    {
                    "quantity": 0,
                    "sku": "string"
                    }
                ],
                "label_id": "string",
                "label_type": "string",
                "remarks": "string",
                "shipped_by": {
                    "email": "string",
                    "id": 0,
                    "name": "string"
                },
                "status": "pending",
                "tracking_numbers": [
                    "string"
                ],
                "updated_at": "2022-09-30T19:39:56.848Z"
                }
            ],
            "shipping_method": "string",
            "status": "created",
            "updated_at": "2022-09-30T19:39:56.848Z",
            "warehouse_remarks": "string",
            "zip": "string"
        }
      ```
* **Sample Call:**
    ```sh
        curl -X 'POST' \
            'https://s2-api.ventmere.io/partner/fulfillment' \
            -H 'accept: application/json' \
            -H 'X-AccessKey: xxxxxxxxxxxxx' \
            -H 'Content-Type: application/json' \
            -d '{
                "address1": "string",
                "address2": "string",
                "address3": "string",
                "city": "string",
                "country_id": "string",
                "fulfillment_warehouse_id": "string",
                "items": [
                    {
                    "quantity": 0,
                    "sku": "string"
                    }
                ],
                "name": "string",
                "phone": "string",
                "province": "string",
                "shipping_method": "standard",
                "zip": "string"
            }'
    ```
