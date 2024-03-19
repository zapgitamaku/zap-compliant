# Verify Business Owner

### POST /v1/owner/verify <a href="#top" id="top"></a>

Allows the Site Admin to add verify business  owner ID details to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to verify a business owner ID.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/owner/verify
```

### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: multipart/form-data'
'Authorization: Bearer  <Bearer Token>'
```

#### For Invited Owners: <a href="#top" id="top"></a>

```
'owner-auth: 63e0f4da81979dcc3b9ee123-1c927684-066d-4c2c-b5c5-a4995f040618'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
it takes both file data and body data

{
      "image": nin.jpg
}

{
    "businessId": "65c4e4945d2869e8324210d8",
    "ownerId": "65c4e4k3942869e8324k3028",
    "documentType": "ID",
    "documentIdType": "vNIN"
    "documentId": "882aa2lp34fa1099",
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |
| owner-auth    | This is the token sent along the invitation link and should be used when invited owner are interacting with platform.   |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="99">Parameter</th><th width="91">Parm Type</th><th width="75">Data Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>image</td><td>Body</td><td>file</td><td>Required</td><td> jpg and png file formats supported</td></tr></tbody></table>

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="122">Parameter</th><th width="73">Param Type</th><th width="86">Data Type</th><th width="100">Required</th><th>Description</th></tr></thead><tbody><tr><td>Owner</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform business owner. firstName, lastName, email, businessId, dob, gender, role, nationality, bvn,  and phoneNumber are required.</td></tr></tbody></table>

#### Business Owner

Contains information about ZAP's platform business owner.

The properties included in the **Owner** object are listed below. All properties are **required** in the request message.

| Property    | Type   | Description                                                                                                    |
| ----------- | ------ | -------------------------------------------------------------------------------------------------------------- |
| businessId  | string | The unique id of the business user.                                                                            |
| firstName   | string | The business owner first name                                                                                  |
| lastName    | string | The business owner last name.                                                                                  |
| email       | string | <p>The business owner unique email address.</p><p>Max length: 320 chars. Standard email pattern.</p>           |
| role        | string | The owner role.                                                                                                |
| bvn         | string | The owner bvn                                                                                                  |
| nationality | string | The owner nationality                                                                                          |
| phoneNumber | string | <p>The business owner phone number.<br>Max length: 15 chars plus country code.<br>Must start with "+" sign</p> |
| dob         | string | The dob of the  owner                                                                                          |
| gender      | string | The gender of the owner                                                                                        |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the newly created business.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 08 Feb 2024 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```
{
    "success": true,
    "data": {
        "message": "Business owner created successfully",
        "ownerId": "65c9ff3b531881155581o74a"
    }
}
```

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
