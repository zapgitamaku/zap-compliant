# Invite Business Owner

### POST /v1/owner/invite <a href="#top" id="top"></a>

Allows a business user to invite a business owner  to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to invite a business owner.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/owner/invite
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "businessId": "65c4e6422b8ca01c66b51110",
    "email": "space@gmail.com"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="102">Parameter</th><th width="73">Param Type</th><th width="94">Data Type</th><th width="104">Required</th><th>Description</th></tr></thead><tbody><tr><td>Owner</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform owner. businessId and email are required.</td></tr></tbody></table>

#### Owner Object

The properties included in the **Owner** object are listed below. All properties are **required** in the request message.

| Property   | Type   | Description                       |
| ---------- | ------ | --------------------------------- |
| businessId | string | The unique business user id.      |
| email      | string | The business owner email address. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the logged in business verification.

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
    "data": "Invitation sent to business owner"
}
```

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
