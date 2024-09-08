## Update Driver

This endpoint updates a driver based on the specific query parameter. Include query parameters such as the driver's name, phone number, and address to update a specific driver.


#1.  Zeo API Request to Update a Driver


The API request body contains all of the necessary information for updating a driver. 


```sh
 curl --location -g --request PUT '{{base_url}}/api/v5/drivers/:driver_id' \
    --header 'Content-Type: application/json' \
    --data-raw '{
      "api_key": "api_key",
      "name": "nishu jain",
      "address": "",
      "phone_no": "8959294300"
    }'
```



#2. Address of the driver

```sh  
"address": "",
```
To update the address of a driver, you need to include the address details in your update request.




#3. Name of the driver
```sh
 "name": "nishu jain",
```
The request body should include the driver's name. To update a new driver, include the driver's name. 



#4. Phone number of driver
```sh
"phone_no": " "
```
The request body should include the driver's phone number. To update a new driver, with the driver's details including phone number.




The command returns JSON in the following format:

```sh
  {
  "code": 200,
  "status": true,
  "message": "Driver updated successfully",
  "data": {
    "driver": {
      "id": 44953,
      "name": "nishu jain",
      "phone_no": "8959294300",
      "address": "delhi",
      "email": "testthird1@gmail.com",
      "active": true
    }
  }
}
```
