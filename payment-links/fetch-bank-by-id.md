# Fetch Bank By Id

### GET /v1/banks/:id <a href="#top" id="top"></a>

Allows the Site Admin to get an available bank on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch a specified bank.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/banks/:id
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Parameter <a href="#samplerequest" id="samplerequest"></a>

| Paramater | Description                |
| --------- | -------------------------- |
| id        | The unique id of the bank. |

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="182">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a owner.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 09 Feb 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "name": "3LINE CARD MANAGEMENT LIMITED",
        "sortCode": "123456",
        "icon": "https://res.cloudinary.com/name/image/upload/v123456/icons/1689243127796.png",
        "createdAt": "2023-07-13T10:44:31.786Z",
        "updatedAt": "2023-08-01T12:01:45.074Z",
        "id": "64afd58f177653c33d9a4220"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name  | Type   | Description                          |
| ----- | ------ | ------------------------------------ |
| banks | Object | Contains information about the bank. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |
