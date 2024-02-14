# Fetch Users By Id

### GET /v1/users/:id <a href="#top" id="top"></a>

Allows the Site Admin to get a user on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a specified of user.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/users/:id
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login</td></tr></tbody></table>

#### UserData Object

Contains information about the specified ZAP platform user.

This array is returned by the following operations:

* #### GET /api/v1/users

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a user.

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
        "name": "ZapAdminUser",
        "email": "adminuser@zap.com",
        "roleId": "63fc98989ffb63cf5cdd0587",
        "iPAddress": [
            "::1"
        ],
        "emailVerified": false,
        "createdAt": "2023-02-27T17:04:00.897Z",
        "updatedAt": "2023-02-27T17:04:00.897Z",
        "id": "63fce280996e16ba19e87185"
        "targetNps": false
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name               | Type    | Description                                                             |
| ------------------ | ------- | ----------------------------------------------------------------------- |
| userData           | Object  | Contains information about the ZAP platform user.                       |
| userData.targetNps | Boolean | if true, user has given NPS for the quarter, if false, collect user NPS |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |

