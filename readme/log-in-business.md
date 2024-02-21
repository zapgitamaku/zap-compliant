# Log In Business

### POST /v1/business/login <a href="#top" id="top"></a>

Allows the Site Admin to log a business  to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to login a business.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/business/login
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
     "email": "myemailaddress@myemail.com",
    "password": "Syx@goal63"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="122">Parameter</th><th width="73">Param Type</th><th width="86">Data Type</th><th width="100">Required</th><th>Description</th></tr></thead><tbody><tr><td>Business</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform business. email, password are required.</td></tr></tbody></table>

#### Business Object

Contains information about ZAP's platform business.

The properties included in the **Business** object are listed below. All properties are **required** in the request message.

| Property | Type   | Description                                                                                                                                     |
| -------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| email    | string | <p>The business user unique email address.</p><p>Max length: 320 chars. Standard email pattern.</p>                                             |
| password | string | <p>The business user password.</p><p>Must contain at least one digit and one special character and it should be between 8 to 30 characters.</p> |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the logged in business.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 08 Feb 2024 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```
{
    "success": true,
    "data": {
        "firstName": "john",
        "lastName": "doe",
        "email": "johndoe@gmail.com",
        "phoneNumber": "2347030839847",
        "phoneNumberVerified": false,
        "bvn": {
            "bvnVerified": false
        },
        "businessName": "Space stocks",
        "numberOfBusinessOwner": 0,
        "numberOfBusinessOwnerFullyVerified": 0,
        "iPAddress": [],
        "emailVerified": false,
        "twoFA": {
            "enabled": false
        },
        "userAgent": [],
        "receiveEmailNotifications": true,
        "transactionVolume": 0,
        "createdAt": "2024-02-08T14:26:28.121Z",
        "updatedAt": "2024-02-08T14:26:28.121Z",
        "id": "65c4e4945d2869e8324210d8",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7Im5hbWUiOiJaYXBVc2VyIiwiZW1haWwiOiJ1c2VyQHphcC5jb20iLCJyb2xlSWQiOiI2M2ZjOTg5ODlmZmI2M2NmNWNkZDA1ODciLCJpUEFkZHJlc3MiOlsiOjoxIl0sImVtYWlsVmVyaWZpZWQiOmZhbHNlLCJjcmVhdGVkQXQiOiIyMDIzLTAyLTI3VDE2OjU3OjA1LjkxM1oiLCJ1cGRhdGVkQXQiOiIyMDIzLTAyLTI3VDE3OjA0OjEyLjIwMloiLCJkZWxldGVkQXQiOiIyMDIzLTAyLTI3VDE3OjA0OjEyLjE5OFoiLCJpZCI6IjYzZmNlMGUxOGI4ZGQ0ZTE2M2QwNmQ1YyJ9LCJpYXQiOjE2Nzc1MjA0MTYsImV4cCI6MTY3NzYwNjgxNn0.aRc7ihhVdZXRIGQtGHGjBhtXbkT_fcyZTd6oUFNz2vM"
    }
}
```

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
