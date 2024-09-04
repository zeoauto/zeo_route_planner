## Create Driver

This endpoint creates a driver based on the specific query parameter. Include query parameters such as the driver's name, phone number, address, and email address to retrieve a specific driver.


##  Zeo API Request to Create Driver


The API request body contains all of the necessary information for creating a driver. 

```sh
 curl --location -g --request POST '{{base_url}}/api/v5/drivers' \
    --header 'Content-Type: application/json' \
    --data-raw '{
      "api_key": "api_key",
      "email": "nishu.jain396@gmail.com",
      "address": "Netaji Subhash Marg, Lal Qila, Chandni Chowk, New Delhi, Delhi 110006",
      "password": "12345678",
      "name": "nishu jain",
      "phone_no": " "
    }'
```    





#1. Email ID of the driver


```sh
"email": "nishu.jain396@gmail.com",
```

This API request provides an email argument for creating a new driver with a given email address. You may verify that the created route is linked to the correct driver by providing the correct email address, resulting in effective delivery or pickup.






#2. Address of the driver


```sh
"address": "Netaji Subhash Marg, Lal Qila, Chandni Chowk, New Delhi, Delhi 110006",
```

To create a new address for the specified driver add street, city, state, and pin code.


#3. Name of the driver

```sh
 "name": "nishu jain",
```
To create a new driver, include the specific driver's name. This ensures that the driver's name is included together with the address

#4. Phone number of driver

```sh
"phone_no": " "
```
The request body should include the driver's phone number. To create a new driver, with the driver's details including phone number.

The command returns JSON in the following format:

```sh
  {
  "code": 200,
  "status": true,
  "message": "Driver created successfully",
  "data": {
    "driver": {
      "id": 44953,
      "email": "john@example.com",
      "name": "John",
      "address": "47 W 13th St, New York, NY 10011, USA",
      "phone_no": "+13239090909090",
      "active": true
    }
  }
}
```
