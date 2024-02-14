# Create User

### POST /v1/users <a href="#top" id="top"></a>

Allows the Site Admin to add a new user to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to create a user.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/users
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "username": "zap_4_life",
    "email": "myemailaddress@myemail.com",
    "password": "P@ssw0rd",
    "phoneNumber": "+2348011111111",
    "roleId": 12345678909876543211235813,
    "referralCode": "zapAffiliate"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="108">Parameter</th><th width="162">Param Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>User</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform user. FirstName, LastName, Email, Password and RoleId are required.</td></tr></tbody></table>

#### User Object

Contains information about ZAP's platform user.

This object is used by the following operations:

* #### POST /api/v1/users

The properties included in the **User** object are listed below. All properties are **required** in the request message.

| Property     | Type   | Description                                                                                                                              |
| ------------ | ------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| username     | string | The unique username picked by the user                                                                                                   |
| email        | string | <p>The user's email address.</p><p>Max length: 320 chars. Standard email pattern.</p>                                                    |
| password     | string | <p>The user's password.</p><p>Must contain at least one digit and one special character and it should be between 8 to 30 characters.</p> |
| roleId       | string | The unique ID for a specific role, optional.                                                                                             |
| referralCode | string | the unique username of a referrer or affiliate                                                                                           |
| phoneNumber  | string | <p>The user's phone number.<br>Max length: 15 chars plus country code.<br>Must start with "+" sign</p>                                   |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the newly created user.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```
{
    "success": true,
    "data": {
        "name": "ShowandTell",
        "email": "show@didnt.com",
        "roleId": "63fc98989ffb63cf5cdd0587",
        "phoneNumber" : "+2348011111111",
        "iPAddress": [
            "::1"
        ],
        "emailVerified": false,
        "createdAt": "2023-02-27T11:54:50.489Z",
        "updatedAt": "2023-02-27T11:54:50.489Z",
        "id": "63fc9a0a29dc8cbccf38d096"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type | Description                                     |
| ---- | ---- | ----------------------------------------------- |
| User | User | Contains information about ZAP's platform user. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

