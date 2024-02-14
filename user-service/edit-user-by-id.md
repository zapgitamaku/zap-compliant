# Edit User By Id

### PUT /v1/users/:id <a href="#top" id="top"></a>

Allows the Site Admin to modify an existing user on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to modify a specified user.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/users/:id
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample** Request Body <a href="#top" id="top"></a>

```json
{
        "name": "ZapAdminAgent",
        "email": "mynew@email.com"
        "viewedTooltipOnMobile": true,
        "viewedTooltipOnWeb": false,
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login</td></tr></tbody></table>

#### UserData Object

Contains updated information about the particular ZAP platform user.

This array is returned by the following operations:

* #### PUT /api/v1/users

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="132">Parameter</th><th width="162">Param Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>User</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform user. FirstName, LastName, Email, Password and RoleId are optional.</td></tr></tbody></table>

#### User Object

Contains information about ZAP's platform user.

This object is used by the following operations:

* #### PUT /api/v1/users

The properties included in the **User** object are listed below. All properties are **optional** in the request message.

| Property | Type   | Description                                                                           |
| -------- | ------ | ------------------------------------------------------------------------------------- |
| name     | string | The name set up by the user.                                                          |
| email    | string | <p>The user's email address.</p><p>Max length: 320 chars. Standard email pattern.</p> |
| roleId   | string | The unique ID for a specific role.                                                    |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with an updated user details.

If the request body contains email, the operation returns a HTTP status code 200, and an otp is generated and sent to the new email. emailVerified is set to false, returns updated user details

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
        "name": "ZapAdminAgent",
        "email": "mynew@email.com",
        "roleId": "63ff98989ffb63cc5cdd0537",
        "iPAddress": [
            "::1"
        ],
        "emailVerified": false,
        "createdAt": "2023-02-27T17:04:00.897Z",
        "updatedAt": "2023-02-27T17:04:00.897Z",
        "id": "63fce280996e16ba19e87185"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name     | Type   | Description                                    |
| -------- | ------ | ---------------------------------------------- |
| userData | Object | Contains information about ZAP platform users. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |

