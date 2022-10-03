# Supplier

You can retrieve a list of all available supplies 

---

## API: Get Suppliers

Learn more : [Specification](https://s2-api.ventmere.io/swagger-ui/#/partner/get_suppliers)

* **URL:**

    `/supplier`

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
            "id": 52,
            "name": "Buckridge, Mills and Bechtelar"
        },
        {
            "id": 29,
            "name": "Buckridge - Streich"
        }
      ]
      ```

* **Sample Call:**
    ```sh
        curl -X 'GET' \
            'https://s2-api.ventmere.io/partner/supplier' \
            -H 'accept: application/json' \
            -H 'X-AccessKey: xxxxxxxxxxxxxxxxxxx'
    ```
