# Create Job Opening

### POST /v1/career <a href="#top" id="top"></a>

Allows zap to add a new job opening on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to Create a new job opening.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/career
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'zap-career: Bearer  ZAP_EXCHANGE_CAREER'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{

    "title": "Backend Engineer",
    "description": "test",
    "location": "remote",
    "type": "full time",
    "qualification": "test",
    "responsibilities": "test",
    "benefits": "nice summer"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description                                      |
| ------------ | ------------------------------------------------ |
| Content-type | application/json                                 |
| zap-career   | This is the special request header key required. |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="166">Parameter</th><th width="98">Parm Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>Career</td><td>Body</td><td>Required</td><td>Contains information about new job on ZAP platform. All fiedls are required.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the new job.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 15 Apr 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "title": "backend engineer",
        "description": "test",
        "location": "remote",
        "type": "full time",
        "qualification": "test",
        "responsibilities": "test",
        "benefits": "nice summer"
        "createdAt": "2024-04-24T20:54:08.494Z",
        "updatedAt": "2024-04-24T20:54:08.494Z",
        "id": "646e79705b646159d3d78d95"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name   | Type   | Description                                         |
| ------ | ------ | --------------------------------------------------- |
| Career | Career | Contains information about new job on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
