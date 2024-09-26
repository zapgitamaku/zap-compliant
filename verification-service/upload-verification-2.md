# Upload Verification(Url)

### POST /v1/verifications/:verificationId/upload-url <a href="#top" id="top"></a>

Allows a User to Upload Verification document with url on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to Upload a verification document via url

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/verifications/verificationId/upload-url
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
      "fileUrl": "data:image/png;base64,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"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="218">Parameter</th><th>Parm Type</th><th width="138">Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>fileUrl</td><td>Body</td><td>string</td><td>Required</td><td>url string</td></tr></tbody></table>

#### Verification Object

Contains information about ZAP's platform user verification data.

This object is used by the following operations:

* **POST /v1/verifications**
* **GET /v1/verifications**
* **GET /v1/verifications/:id**
* **POST /v1/verifications/userid/upload-image**
* **GET /v1/verifications/userid/:id**
* **PUT /v1/verifications/:id**
* **DELETE /v1/verifications/:id**

The properties included in the **Verifications** object are listed below.

| Property         | Type     | Description                                                                                    |
| ---------------- | -------- | ---------------------------------------------------------------------------------------------- |
| id               | String   | The unique ID for a specific Verification. Used in Response                                    |
| userId           | String   | The unique ID of the User.                                                                     |
| documentType     | String   | ID or residence                                                                                |
| documentUrl      | String   | Link to uploaded document                                                                      |
| status           | String   | Verification status                                                                            |
| expirationDate   | Date     | Expiry date of document                                                                        |
| comments         | String   | Optional reviewer's comment                                                                    |
| verificationDate | Date     | Date of verification                                                                           |
| reviewer         | String   | Reviewer identity                                                                              |
| reviewDate       | Date     | Date of review                                                                                 |
| createdAt        | dateTime | This property displays when the verification was created. Used only in response messages.      |
| updatedAt        | dateTime | This property displays when the verification was last updated. Used only in response messages. |

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
    "data": {
        "userId": "6410e2b1bc3d3821133a90f9",
        "documentId": "12345asdfgh112",
        "documentType": "residence",
        "documentUrl": "https://res.cloudinary.com/dukdbbrbc/image/upload/v1679260911/user-verification/IMG_1287.jpg",
        "status": "pending",
        "comments": "",
        "createdAt": "2023-03-17T10:11:43.565Z",
        "updatedAt": "2023-03-19T22:27:55.511Z",
        "id": "64143cdf1760eaf60a2a4dd6"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name         | Type         | Description                                               |
| ------------ | ------------ | --------------------------------------------------------- |
| Verification | verification | Contains information about Verifications on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 401  | Unauthorized                                                                                                                                                                                                                                                                                                                      |
| 404  | Not Found: Returned if the request                                                                                                                                                                                                                                                                                                |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
