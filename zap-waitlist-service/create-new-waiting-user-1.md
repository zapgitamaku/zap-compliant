# Add New User to Newsletter List

### POST /v1/subscribe <a href="#top" id="top"></a>

Add a new user to the newsletter.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to add a new user to the newsletter.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/subscribe
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
      "name": "sunlight"
      "email": "sunlight@gmail.com",
      "isBeginner": true
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="142">Parameter</th><th width="124">Parm Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>string</td><td>Required</td><td>contains the user's name</td></tr><tr><td>email</td><td>string</td><td>Required</td><td>contains the user's valid email</td></tr><tr><td>isBeginner</td><td>boolean</td><td>Required</td><td>determines the category of the user</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200 | 201, with information about the newly added user.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Thur, 10 May 2023 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
      "success": true,
      "data": "New user added successfully"
    }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
