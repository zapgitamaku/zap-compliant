# Refresh Business Token

### POST /v1/business/refreshToken <a href="#top" id="top"></a>

Allows the Site Admin to refresh the logged in user token for access  to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to refresh business access token

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/business/refreshToken
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "refreshToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImdpZGVvbkB6YXAuYWZyaWNhIiwiaWQiOiI2NWYxZmZiOTQ1M2NjYTc0MjFkZDA4ZmIiLCJpYXQiOjE3MTEwOTkwOTgsImV4cCI6MTcxMTE4NTQ5OH0.XfqajLiSU3tfyEl-GG_gwV82NLvp8FuVE0k9t9VbT2c"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="122">Parameter</th><th width="73">Param Type</th><th width="86">Data Type</th><th width="100">Required</th><th>Description</th></tr></thead><tbody><tr><td>Business</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform business. refreshToken, is required.</td></tr></tbody></table>

#### Business Object

Contains information about ZAP's platform business.

The properties included in the **Business** object are listed below. All properties are **required** in the request message.

| Property     | Type   | Description                             |
| ------------ | ------ | --------------------------------------- |
| refreshToken | string | The business user refresh access token. |

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
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImdpZGVvbkB6YXAuYWZyaWNhIiwiaWQiOiI2NWYxZmZiOTQ1M2NjYTc0MjFkZDA4ZmIiLCJpYXQiOjE3MTEwOTk2MTgsImV4cCI6MTcxMTEyMTIxOH0.bEScIv54iZHZRe7V20EQhl8ncjbcHLKJdl9h2vrpbPE"
    }
}
```

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
