# Create Business Owner

### POST /v1/owner <a href="#top" id="top"></a>

Allows the Site Admin to add a new business  owner to the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to create a business owner.

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/owner
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "businessId": "65c4e4945d2869e8324210d8",
    "firstName": "john",
    "lastName": "doe",
    "email": "johndoe@gmail.com",
    "phoneNumber": "2347030839847",
    "gender": "male",
    "nationality": "nigerian",
    "role": "shareholder"
    "bvn": "12345567788",
    "state": "lagos",
    "city": "ikeja",
    "country": "nigeria",
    "address": "no,1 3j33",
    "dob": "1980-08-12"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                             |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                                        |
| Authorization | This is the ZAP Business API Platform authorization token, and must be sent with every API request that requires login. |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="122">Parameter</th><th width="73">Param Type</th><th width="86">Data Type</th><th width="100">Required</th><th>Description</th></tr></thead><tbody><tr><td>Owner</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about ZAP platform business owner. firstName, lastName, email, businessId, dob, gender, role, nationality, bvn,  and phoneNumber are required.</td></tr></tbody></table>

#### Business Object

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
