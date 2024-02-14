# Delete Verification by Id

### DELETE /v1/verification <a href="#top" id="top"></a>

Allows a User to delete verification data on the platform.

#### HTTP Method <a href="#top" id="top"></a>

DELETE

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to delete verification data.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/verifications/:Id
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="261">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>Verification</td><td>Body</td><td>Verification</td><td>Required</td><td>Contains information about  Verification data on ZAP platform userId, documentType and documentUrl are required.</td></tr></tbody></table>

#### Verification Object

Contains information about ZAP's platform user verification data.

This object is used by the following operations:

* #### POST /v1/verifications
* #### GET /v1/verifications
* #### GET /v1/verifications/:id
* #### GET /v1/verifications/userid/:id
* #### PUT /v1/verifications/:id
* #### DELETE /v1/verifications/:id

The properties included in the **Verifications** object are listed below.

| Property         | Type     | Description                                                                                    |
| ---------------- | -------- | ---------------------------------------------------------------------------------------------- |
| id               | String   | The unique ID for a specific Verification. Used in Response                                    |
| userId           | String   | The unique ID of the User.                                                                     |
| documentType     | String   |                                                                                                |
| documentUrl      | String   |                                                                                                |
| status           | String   |                                                                                                |
| expirationDate   | Date     |                                                                                                |
| comments         | String   |                                                                                                |
| verificationDate | Date     |                                                                                                |
| reviewer         | String   |                                                                                                |
| reviewDate       | Date     |                                                                                                |
| createdAt        | dateTime | This property displays when the verification was created. Used only in response messages.      |
| updatedAt        | dateTime | This property displays when the verification was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the deletion.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": "Verification deleted successfully"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name         | Type         | Description                                                 |
| ------------ | ------------ | ----------------------------------------------------------- |
| Verification | Verification | Contains information about  Verifications on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

