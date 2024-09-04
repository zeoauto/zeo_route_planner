## Get all drivers

Fleet managers who oversee many drivers can access all of them through this endpoint. Using this endpoint, they can obtain information about all the drivers

Request an API that collects data about every driver.

**Submit the API request**

```sh
curl --location -g --request GET '{{base_url}}/api/v5/drivers?api_key=api_key'```


The request is directed to the /driver's endpoint of your API.
This header is required to authenticate the request.
The response typically includes a list of drivers with relevant details like ID, name, email, address, and phone.


Here's what Zeo’s API request looks like for getting a list of all drivers:

The command above generates the following JSON structure:

```sh
  {
  "code": 200,
  "status": true,
  "message": "success",
  "data": {
    "drivers": [
      {
        "id": 44914,
        "email": "0f12ebdd@gmail.com",
        "name": "nishu jain",
        "address": null,
        "phone_no": "8959294300",
        "active": true
      }
    ]
  }
}
```
