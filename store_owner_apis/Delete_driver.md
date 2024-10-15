## Delete Driver

SThis endpoint deletes a driver based on the specific query parameter. Include the driver_id query parameter as instructed to eliminate a particular driver.

## Zeo API Request to Delete a Driver

The Zeo API request body contains all the necessary information for deleting a driver. 



```sh
  curl --location -g --request DELETE '{{base_url}}/api/v5/drivers/:driver_id' \
    --header 'Content-Type: application/json' \
    --data-raw '{
      "api_key": "api_key"
    }'

```

## Driver_id

Get  the driver's unique ID to delete a specific driver. The driver's unique ID is the information you wish to remove.



```sh
'{{base_url}}/api/v5/drivers/:driver_id' \
```
To delete a driver using the Zeo Route Planner API, send an HTTP DELETE request to the appropriate endpoint. The request will delete the driver from the system, and a confirmation response should be sent to ensure that the deletion was successful.


The command returns JSON in the following format:



```sh
{
    "code": 200,
    "status": true,
    "message": "Driver deleted successfully"
  }

```
