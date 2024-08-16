# Update Support Command  by id

### PUT /v1/supportCommand/:id <a href="#top" id="top"></a>

Allows the support user to modify a support command by id on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a support user request to modify a support command by id.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/supportCommand/:id
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
      "message": "Thanks for the help", // optional
      "command": "/thanks" // optional
};
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="142">Parameter</th><th width="91">Parm Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>Support Command</td><td>Body</td><td>Optional</td><td>Contains information about creating support messages on ZAP platform. message, and command are optional.</td></tr></tbody></table>

The properties included in the Support Command object are listed below.

<table><thead><tr><th>Property</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td>messages</td><td>string</td><td>The message of the support command.</td></tr><tr><td>command</td><td>string</td><td>The support command name.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the success message.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Thur, 25 Apr 2024 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
      "success": true,
      "data": "Support Command Updated Successfully"
    }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name            | Type            | Description                                        |
| --------------- | --------------- | -------------------------------------------------- |
| Support Command | Support Command | Contains updated  support command success message. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
