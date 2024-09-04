## Store owner APIs

Store owners can use store owner APIs to automatically manage their stores, products, orders, and other relevant processes. These APIs are often offered by delivery services or e-commerce platforms. Store owners may automate operations, integrate their shopfronts with other services, and run their enterprises more profitably.

Manage your fleet, assign duties, and give customers and other stakeholders real-time updates by collecting driver data via an API.

## Create stops

Stops are created by this endpoint. This endpoint retrieves the drivers using the API, and it is possible to change the same profile later.

While using an API for route creation or optimization, specifying a stop address is crucial. Depending on the API, you can provide the stop address in various formats, such as the full address or geographic coordinates (latitude and longitude). Here's how you can specify stop addresses and other details for an API.


#1. Stop Address Formates

```sh
 "address": "Gwalior Madhya Pradesh",
```

**Use Case:** The address of the stop location. You can provide the street address,  including the name of the street and the state


Geographic Coordinates (Latitude and Longitude)

```sh
"latitude": 0,
"longitude": 0.0,
```
**Use Case:** When you have a location's precise coordinates—which are sometimes more accurate than an address—you use this format.


#2. Stop duration and stop date 


```sh
 "stop_duration": 5,
 "stop_date": "2022-03-10",
```

Including parameters like stop_duration and stop_date can help customize the routing process. It specifies how long the driver will stay at each stop and on what date the stop is scheduled.



#3. Parcel count


```sh
 "parcel_count": 2,
```

To indicate how many shipments or parcels are connected to each stop, the parcel_count option is frequently used. Considering the number of deliveries or pickups that must be made at each site may help in route optimization. 

With this data, the API can then allocate the load among drivers fairly, maximize vehicle capacity, or give stops with larger parcel counts priority.


#4. Define time windows for each stop


```sh
 "arrive_start": "now",
 "arrive_end": "anytime",
 "earliest": 0,
 "latest": 0,
```


To specify time ranges for each stop, utilize the API's arrive_start, arrive_end, earliest, and latest options. It assists in ensuring that pickups and deliveries happen within the allotted time,  which can be critical for time-sensitive operations.
 
#5.  Driver id

```sh
  "driver_id": "",
```

To assign a specific driver to a route,  this API request includes the driver_id argument. You can ensure that the generated route is linked to the right driver by providing the driver_id, which enables more organized and effective delivery or pickup.



 #6. Stop type

```sh
"stop_type": "delivery",
```

The stop_type parameter in an API request for route creation indicates whether it is a delivery, pickup, or both. By doing this, the routing algorithm is better able to comprehend the goal of each stop and adjust the route accordingly.



#7. Customer Details

```sh
"customer_name": "nishu",
"customer_mobile_number": "+911234567890",
"customer_email": "",
```

Customize your delivery or pickup processes by using customer-specific information such as customer_name, customer_mobile_number, and customer_email. These details are usually linked to every destination along the route, helping the driver identify and communicate with the client.

## How to use Zeo API to create stops


Get Zeo Route Optimization API
To authenticate your requests, verify that you have an access token or API key.


### Make the data organized


**Stops:** Compile a list of addresses of stops, stop duration, stop date,  geographic coordinates (longitude and latitude) stop type, parcel count, driver_id, and customer details for each stop on the route.


### Submit the API request

**HTTP Method:** When building a route, you usually use a POST request.

You must use a written code that sends an HTTP request to the API endpoint with the required information to submit an API request to generate a stop. 



##### For example: For Zeo API to create stops,

```sh
curl --location --request POST '{{base_url}}/api/v5/route_stop' \
--header 'Content-Type: application/json' \
--data-raw '{
    "api_key": "api_key",
    "stops": [
        {
            "address": "Gwalior Madhya Pradesh",
            "latitude": 0,
            "longitude": 0.0,
            "notes": "dsf",
            "optimize_status": "normal",
            "stop_duration": 5,
            "stop_date": "2022-03-10",
            "parcel_count": 2,
            "arrive_start": "now",
            "arrive_end": "anytime",
            "earliest": 0,
            "latest": 0,
            "driver_id": "",
            "stop_type": "delivery",
            "customer_name": "nishu",
            "customer_mobile_number": "+911234567890",
            "customer_email": "",
            "metadata": [{}]
        }
    ]
}'
```
