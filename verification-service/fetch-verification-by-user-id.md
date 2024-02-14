# Fetch Verification by user Id

### GET /v1/verifications/userId/:Id <a href="#top" id="top"></a>

Allows a User to get verification data by user id on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get verification data.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/verifications/userId/:Id
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

| Key | Value  | Description                         |
| --- | ------ | ----------------------------------- |
| Id  | \<Id>  | The unique ID for a specific user.  |

####

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the specified verification.

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
    "data": {
                "userId": "6410e2b1bc3d3821133a90f9",
                "documentId": "12345asdfgh112",
                "documentType": "residence",
                "documentUrl": "https://res.cloudinary.com/dwwttestc/image/upload/v16793435355/user-verification/09-3.jpg",
                "status": "pending",
                "comments": "",
                "createdAt": "2023-03-17T10:11:43.565Z",
                "updatedAt": "2023-03-22T03:05:09.603Z",
                "id": "64143cdf122356ace4dd6"
    }
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

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

