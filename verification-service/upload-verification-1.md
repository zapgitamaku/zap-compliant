# Upload Verification(get file url)



Allows a User to Upload Verification document on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to Upload a verification document.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/verifications/getFileUrl
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request form body** <a href="#top" id="top"></a>

```json
{
      "file": file.jpg
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="218">Parameter</th><th>Parm Type</th><th width="138">Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>file</td><td>Body</td><td>file</td><td>Required</td><td>jpg, png, jpeg image format supported</td></tr></tbody></table>



The properties included in the **Verifications** object are listed below.

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the updated verification.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Tue, 28 Feb 2023 02:10:15 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": "https://zap.africa.s3.eu-north-1.amazonaws.com/verification-documents/a0d873eac95753d9a263fa05d543ed99.jpeg"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type   | Description                                      |
| ---- | ------ | ------------------------------------------------ |
| Data | String | Contains url of the file uploaded to zap server. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 401  | Unauthorized                                                                                                                                                                                                                                                                                                                      |
| 404  | Not Found: Returned if the request                                                                                                                                                                                                                                                                                                |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
