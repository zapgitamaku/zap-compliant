# Upload Verification

### POST /v1/verifications <a href="#top" id="top"></a>

Allows a User to Upload Verification document on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to Upload a verification document.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/verifications/verificationId/upload-image
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
      "image": file.jpg
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="218">Parameter</th><th>Parm Type</th><th width="138">Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>image</td><td>Body</td><td>file</td><td>Required</td><td>jpg, png, jpeg image format supported</td></tr></tbody></table>

#### Verification Object

Contains information about ZAP's platform user verification data.

This object is used by the following operations:

* #### POST /v1/verifications
* #### GET /v1/verifications
* #### GET /v1/verifications/:id
* #### POST /v1/verifications/userid/upload-image
* #### GET /v1/verifications/userid/:id
* #### PUT /v1/verifications/:id
* #### DELETE /v1/verifications/:id

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

<pre class="language-json"><code class="lang-json">{
    "success": true,
    "data":
<strong>        {
</strong>        "userId": "6910f2b1bc3c1821133a20f9",
        "documentId": "12345asdfgh112",
        "documentType": "residence",
        "documentUrl": "https://res.cloudinary.com/testcluster/image/upload/v16722819911/user-verification/file.jpg",
        "status": "pending",
        "comments": "",
        "createdAt": "2023-03-17T10:11:43.565Z",
        "updatedAt": "2023-03-19T22:27:55.511Z",
        "id": "64942cdf176abaf60a2d4dd6"
    }
}
</code></pre>

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name         | Type         | Description                                                 |
| ------------ | ------------ | ----------------------------------------------------------- |
| Verification | verification | Contains information about  Verifications on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 401  | Unauthorized                                                                                                                                                                                                                                                                                                                      |
| 404  | Not Found: Returned if the request                                                                                                                                                                                                                                                                                                |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

