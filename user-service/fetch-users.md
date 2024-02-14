# Fetch Users

### GET /v1/users <a href="#top" id="top"></a>

Allows the Site Admin to get a list of users on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a list of users.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/users/?bodyLimit=1&pageLimit=3&startDate&endDate
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### &#x20;**Sample request query** <a href="#top" id="top"></a>

<table><thead><tr><th width="242">Key</th><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>bodyLimit</td><td>1</td><td>Optional query parameter that specifies the number of users in the response body</td></tr><tr><td>pageLimit</td><td>3</td><td>Optional query parameter that paginates the list of users in the response body</td></tr><tr><td>startDate</td><td></td><td>Optional query parameter that adds a start date range to the list of users in the response body</td></tr><tr><td>endDate</td><td></td><td>Optional query parameter that adds a end date range to the list of users in the response body</td></tr></tbody></table>

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login</td></tr></tbody></table>

#### UserData Array

Contains information about ZAP platform users.

This array is returned by the following operations:

* #### GET /api/v1/users

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a list of users.

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
        "userData": [
            {
                "name": "Zap",
                "email": "superuser@zap.com",
                "roleId": "63fc98989ffb63cf5cdd0587",
                "iPAddress": [
                    "::1"
                ],
                "emailVerified": false,
                "createdAt": "2023-02-27T16:56:45.283Z",
                "updatedAt": "2023-02-27T16:56:45.283Z",
                "id": "63fce0cd8b8dd4e163d06d55"
            }
        ],
        "bodyLimit": 1,
        "pageLimit": 3,
        "dataCount": 3
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name     | Type  | Description                                    |
| -------- | ----- | ---------------------------------------------- |
| userData | Array | Contains information about ZAP platform users. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |

