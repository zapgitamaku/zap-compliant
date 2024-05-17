# Fetch All Jobs

### GET /v1/career/all <a href="#top" id="top"></a>

Allows individual to get all available zap job openings on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get all job openings.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/career/all
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the job openings.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 15 Apr 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": [
        {
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
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name   | Type   | Description                                              |
| ------ | ------ | -------------------------------------------------------- |
| Career | Career | Contains information about job openings on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
