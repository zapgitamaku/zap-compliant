# Fetch Active Loyalty Program

### GET /v1/loyaltyProgram/active <a href="#top" id="top"></a>

Allows a zap user to get the active loyalty program on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get the active loyalty program.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/loyaltyProgram
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

#### LoyaltyProgram Object

Contains information about ZAP's platform loyalty programs.

<table><thead><tr><th>Property</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The unique ID for a specific loyalty program.</td></tr><tr><td>name</td><td>string</td><td>The name of the program.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the loyalty program.

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
    "data": {
        "name": "Test Loyalty Program.",
        "isEnded": false,
        "createdAt": "2024-06-26T01:45:03.830Z",
        "updatedAt": "2024-08-01T12:39:35.988Z",
        "endingDate": "2024-08-01T19:00:00.830Z",
        "id": "667b729f555588230fd76f59"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name           | Type           | Description                                               |
| -------------- | -------------- | --------------------------------------------------------- |
| LoyaltyProgram | LoyaltyProgram | Contains information about auto messages on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
