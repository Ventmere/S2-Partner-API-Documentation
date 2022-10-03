# Product
Product resource let you fetch all your available products.

---

## API: Get Products

Learn more : [Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/query_products)

* **URL:**

    `/product`

* **Method:**

    `GET`

* **URL Params**

| Parameter | Required | Description |
| ------ | ------ | ----- |
| `next_token` | No | A token for use in pagination. Your subsequent call can include `next_token=xxxxx` in order to fetch the next page of the list |

* **Data Params**

    `None`

* **Success Response**

    * **Code:** `200` <br />
      **Content:**
      ```json
      {
        "item":[
            {
                "sku": "mluw-tb2n",
                "upc": "7990611084",
                "title": "Licensed Cotton Keyboard",
                "is_parent": false,
                "remarks": "{\"masked_data\":\"masked\"}",
                "case_pack": 10,
                "image_main": "https://loremflickr.com/640/480",
                "package_length_mm": 225,
                "package_width_mm": 97,
                "package_height_mm": 264,
                "shipping_weight_kg": 0.65,
                "case_length_mm": 508,
                "case_width_mm": 286,
                "case_height_mm": 489,
                "case_weight_kg": 7.96,
                "category": "Headphones"
            }
        ]
      }
      ```

* **Sample Call:**
    ```sh
        curl -X 'GET' \
            'https://s2-api.ventmere.io/partner/product' \
            -H 'accept: application/json' \
            -H 'X-AccessKey: xxxxxxxxxxxxx'
    ```