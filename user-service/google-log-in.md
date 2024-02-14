# Google Log In

### GET /v1/users/auth/google <a href="#top" id="top"></a>

Allows the Site Admin to log a user in to the platform with google auth.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to log a user in using google.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/users/auth/google
```

After calling this endpoint and the google authentication is successful.\
The client will be redirected to a page with url format:

```
http://frontendURL/auth/success?sessionId=sessionId
```

The client will then extract this sessionId, and make a call to

```
https://{hostname}/v1/users/auth/session?sessionId=sessionId
```

Where the query parameter "sessionId" is the sessionId extracted from the url

The response will be a user object containing the user details, the access and the refresh tokens, if the sessionId is valid.

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

#### User Object

Contains information about ZAP's platform user.

This object is used by the following operations:

* #### GET /api/v1/users

The properties included in the **User** object are listed below. All properties are **required** in the request message.

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the new user.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```
{
    "success": true,
    "data": {
        "success": true,
        "data": {
            "name": "ZapUser",
            "email": "user@zap.com",
            "roleId": "63fc98989ffb63cf5cdd0587",
            "iPAddress": [
                "::1"
            ],
            "emailVerified": false,
            "createdAt": "2023-02-27T16:57:05.913Z",
            "updatedAt": "2023-02-27T17:04:12.202Z",
            "deletedAt": "2023-02-27T17:04:12.198Z",
            "id": "63fce0e18b8dd4e163d06d5c"
        },
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7Im5hbWUiOiJaYXBVc2VyIiwiZW1haWwiOiJ1c2VyQHphcC5jb20iLCJyb2xlSWQiOiI2M2ZjOTg5ODlmZmI2M2NmNWNkZDA1ODciLCJpUEFkZHJlc3MiOlsiOjoxIl0sImVtYWlsVmVyaWZpZWQiOmZhbHNlLCJjcmVhdGVkQXQiOiIyMDIzLTAyLTI3VDE2OjU3OjA1LjkxM1oiLCJ1cGRhdGVkQXQiOiIyMDIzLTAyLTI3VDE3OjA0OjEyLjIwMloiLCJkZWxldGVkQXQiOiIyMDIzLTAyLTI3VDE3OjA0OjEyLjE5OFoiLCJpZCI6IjYzZmNlMGUxOGI4ZGQ0ZTE2M2QwNmQ1YyJ9LCJpYXQiOjE2Nzc1MjA0MTYsImV4cCI6MTY3NzYwNjgxNn0.aRc7ihhVdZXRIGQtGHGjBhtXbkT_fcyZTd6oUFNz2vM"
        "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7Im5hbWUiOiJaYXBVc2VyIiwiZW1haWwiOiJ1c2VyQHphcC5jb20iLCJyb2xlSWQiOiI2M2ZjOTg5ODlmZmI2M2NmNWNkZDA1ODciLCJpUEFkZHJlc3MiOlsiOjoxIl0sImVtYWlsVmVyaWZpZWQiOmZhbHNlLCJjcmVhdGVkQXQiOiIyMDIzLTAyLTI3VDE2OjU3OjA1LjkxM1oiLCJ1cGRhdGVkQXQiOiIyMDIzLTAyLTI3VDE3OjA0OjEyLjIwMloiLCJkZWxldGVkQXQiOiIyMDIzLTAyLTI3VDE3OjA0OjEyLjE5OFoiLCJpZCI6IjYzZmNlMGUxOGI4ZGQ0ZTE2M2QwNmQ1YyJ9LCJpYXQiOjE2Nzc1MjA0MTYsImV4cCI6MTY3NzYwNjgxNn0.aRc7ihhVdZXRIGQtGHGjBhtXbkT_fcyZTd6oUFNz2vM"
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

