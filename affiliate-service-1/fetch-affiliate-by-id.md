# Fetch User Activities Log

### GET /v1/activity/user/all/:userId?bodyLimit=50\&pageLimit=1 <a href="#top" id="top"></a>

Allows a zap user to fetch all their activities log

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch activity log

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/activity/user/all/:userId
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login</td></tr></tbody></table>

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

| Key    | Value | Description                        |
| ------ | ----- | ---------------------------------- |
| userId | \<Id> | The unique ID for the zap user id. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with the activities log.

<table><thead><tr><th width="190.33333333333331">Property</th><th width="333">Type</th><th>Description</th></tr></thead><tbody><tr><td>activity</td><td>String</td><td>The activity type and it can have a value of login, logout, changes, bankAccount, order, swap, verification, reactivate, deactivate.</td></tr><tr><td>userId</td><td>String</td><td>The unique ID for a specific user.</td></tr><tr><td>description</td><td>String</td><td>The activity description.</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the activity was created.</td></tr></tbody></table>

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 12 Sep 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "activities": [
            {
                "userId": "6515a38ef6d2985656496941",
                "activity": "login",
                "description": "You Logged into your account from  Lagos, Nigeria using PostmanRuntime/7.41.2",
                "iPAddress": "::1",
                "userAgent": "PostmanRuntime/7.41.2",
                "newDevice": false,
                "createdAt": "2024-08-27T02:25:29.327Z",
                "updatedAt": "2024-08-27T02:25:29.327Z",
                "id": "66cd3919ce8803f7e029761f"
            },
            {
                "userId": "6515a38ef6d2985656496941",
                "activity": "login",
                "description": "You Logged into your account from  Lagos, Nigeria using PostmanRuntime/7.41.2",
                "iPAddress": "::1",
                "userAgent": "PostmanRuntime/7.41.2",
                "newDevice": false,
                "createdAt": "2024-08-27T02:23:11.379Z",
                "updatedAt": "2024-08-27T02:23:11.379Z",
                "id": "66cd388f1fd6aaf1e04fbc47"
            }
        ],
        "count": 2
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
