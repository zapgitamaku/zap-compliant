# Fetch System Notifications

### GET /v1/notification <a href="#top" id="top"></a>

Allows an admin User to get a list of all  (if no filter query - system) notifications on retool.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a list of system notifications.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/notification
```

#### **Sample request query** <a href="#top" id="top"></a>

<table><thead><tr><th width="172">Key</th><th width="104">Value</th><th>Description</th></tr></thead><tbody><tr><td>bodyLimit</td><td>50</td><td>Optional query parameter that specifies the number of notification in the response body</td></tr><tr><td>pageLimit</td><td>1</td><td>Optional query parameter that paginates the list of notifications in the response body</td></tr></tbody></table>

## &#x20; <a href="#samplerequest" id="samplerequest"></a>

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |



## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the notifications.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "activityData": [
            {
                "description": "System notification for the server",
                "type": "system",
                "topic": "System Notification",
                "createdAt": "2023-11-8T12:52:50.345Z",
                "updatedAt": "2023-11-8T12:52:50.345Z",
                "id": "63fdf9229c58e23ee6f80de1"
            }
        ],
        "bodyLimit": 50,
        "pageLimit": 1,
        "dataCount": 4
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description                    |
| ------------ | ------------------------------ |
| Content-Type | application/json charset=utf-8 |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name             | Type  | Description                                                   |
| ---------------- | ----- | ------------------------------------------------------------- |
| NotificationData | array | Contains objects containing information  about notifications. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

