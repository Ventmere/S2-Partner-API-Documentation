# Inventory Supply

Inventory supply returns the quantities of the inventory items for a specified warehouse <br />
<br />

---

## Get Inventory Supply

Learn more : [Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/get_inventory_supply)

* **URL:**

    `/inventory-supply`

* **Method:**

    `GET`

* **URL Params**

| Parameter | Required | Description |
| ------ | ------ | ----- |
| `warehouse_id` | Yes | The id of the warehouse |
| `sku_list` | No | The list of SKU for fetching their inventory |

* **Data Params**

    `None`

* **Success Response**

    * **Code:** `200` <br />
      **Content:**
      ```json
        [
            {
                "sku": "h516-ozd4",
                "quantity_avaliable": 0,
                "quantity_pending": 0,
                "quantity_hold": 0
            },
            {
                "sku": "j40c-20s3",
                "quantity_avaliable": 0,
                "quantity_pending": 0,
                "quantity_hold": 0
            },
            {
                "sku": "pnb6-7w26",
                "quantity_avaliable": 0,
                "quantity_pending": 0,
                "quantity_hold": 0
            }
        ]
      ```

* **Sample Call:**

```sh
    curl -X 'GET' \
        'https://s2-api.ventmere.io/partner/inventory-supply?warehouse_id=system_69' \
        -H 'accept: application/json' \
        -H 'X-AccessKey: xxxxxxxxxxxxx'
```