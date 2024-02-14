# Refresh User Token

### POST /v1/refresh <a href="#top" id="top"></a>

Allows the user to refresh their access token on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to refresh the user's token

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/refresh
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
    "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7Im5hbWUiOiJaYXBVc2VyIiwiZW1haWwiOiJ1c2VyQHphcC5jb20iLCJyb2xlSWQiOiI2M2ZjOTg5ODlmZmI2M2NmNWNkZDA1ODciLCJpUEFkZHJlc3MiOlsiOjoxIl0sImVtYWlsVmVyaWZpZWQiOmZhbHNlLCJjcmVhdGVkQXQiOiIyMDIzLTAyLTI3VDE2OjU3OjA1LjkxM1oiLCJ1cGRhdGVkQXQiOiIyMDIzLTAyLTI3VDE3OjA0OjEyLjIwMloiLCJkZWxldGVkQXQiOiIyMDIzLTAyLTI3VDE3OjA0OjEyLjE5OFoiLCJpZCI6IjYzZmNlMGUxOGI4ZGQ0ZTE2M2QwNmQ1YyJ9LCJpYXQiOjE2Nzc1MjA0MTYsImV4cCI6MTY3NzYwNjgxNn0.aRc7ihhVdZXRIGQtGHGjBhtXbkT_fcyZTd6oUFNz2vM"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="159">Parameter</th><th width="162">Param Type</th><th width="119">Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>refreshToken</td><td>Body</td><td>String</td><td>Required</td><td>Contains the refreshToken obtained when the user logged in, required. Expires in 4hrs</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the new token.

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
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7Im5hbWUiOiJaYXBVc2VyIiwiZW1haWwiOiJ1c2VyQHphcC5jb20iLCJyb2xlSWQiOiI2M2ZjOTg5ODlmZmI2M2NmNWNkZDA1ODciLCJpUEFkZHJlc3MiOlsiOjoxIl0sImVtYWlsVmVyaWZpZWQiOmZhbHNlLCJjcmVhdGVkQXQiOiIyMDIzLTAyLTI3VDE2OjU3OjA1LjkxM1oiLCJ1cGRhdGVkQXQiOiIyMDIzLTAyLTI3VDE3OjA0OjEyLjIwMloiLCJkZWxldGVkQXQiOiIyMDIzLTAyLTI3VDE3OjA0OjEyLjE5OFoiLCJpZCI6IjYzZmNlMGUxOGI4ZGQ0ZTE2M2QwNmQ1YyJ9LCJpYXQiOjE2Nzc1MjA0MTYsImV4cCI6MTY3NzYwNjgxNn0.aRc7ihhVdZXRIGQtGHGjBhtXbkT_fcyZTd6oUFNz2vM"
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

