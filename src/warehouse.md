# Warehouse

You can retrieve a list of all available warehouses

---

## API: Get Warehouses

Learn more : [Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/get_warehouses)

* **URL:**

    `/warehouse`

* **Method:**

    `GET`

* **URL Params:**

    `None`

* **Data Params:**

    `None`

* **Success Response:**

    * **Code** `200` <br />
      **Content:**
      ```json
        [
            {
                "id": "system_73",
                "name": "Bailey, Prosacco and Quigley"
            },
            {
                "id": "system_51",
                "name": "Bartoletti, Mueller and Gerhold"
            },
            {
                "id": "system_87",
                "name": "Berge, Heathcote and Langosh"
            }
        ]
      ```

* **Sample Call:**
    ```sh
        curl -X 'GET' \
            'https://s2-api.ventmere.io/partner/warehouse' \
            -H 'accept: application/json' \
            -H 'X-AccessKey: xxxxxxxxxxxxxxxxxxx'
    ```