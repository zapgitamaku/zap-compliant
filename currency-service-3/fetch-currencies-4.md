# Delete Specific User Alerts

### DELETE /v1/priceAlerts/delete/:alertId <a href="#top" id="top"></a>

Allows a zap user to delete an alert on the platform.

#### HTTP Method <a href="#top" id="top"></a>

DELETE

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to delete a user alerts.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/priceAlerts/delete/:alertId
```

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

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="163">key</th><th width="173">value</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>&#x3C;userid></td><td>The unique ID of the user.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the user preferences.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 15 Jun 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": "Alert deleted successfully"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name        | Type        | Description                                                 |
| ----------- | ----------- | ----------------------------------------------------------- |
| PriceAlerts | PriceAlerts | Contains information about user preference on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
