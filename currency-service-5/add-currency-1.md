# Application to Job Opening

### POST /v1/career/submit <a href="#top" id="top"></a>

Allows interested individuals to apply to a job opening on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to apply to a new job opening.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/career/submit
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: multipart/form-data'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
a form data for both cv file data (only pdf allowed) and text data.
{
    "cv": "cv.pdf",
   "firstName": "John",
   "lastName": "doe",
   "jobId": "662bd9239d74785eaf438df7",
   "phoneNumber": "07012345678",
   "email": "joedoe@gmail.com",
   "startDate": "01-01-2024",
   "coverLetter": "test",
   "education":  "bsc",
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description         |
| ------------ | ------------------- |
| Content-type | multipart/form-data |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="166">Parameter</th><th width="98">Parm Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>Application</td><td>Body</td><td>Required</td><td>Contains information about new job on ZAP platform. All fiedls are required except coverLetter.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with success message

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
    "data": "Application Submitted Successfully"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name        | Type        | Description               |
| ----------- | ----------- | ------------------------- |
| Application | Application | Contains success message. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
