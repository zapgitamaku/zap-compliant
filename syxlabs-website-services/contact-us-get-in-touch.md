# Contact Us (get in touch)

### POST /v1/contactus <a href="#top" id="top"></a>

Allows an entity to contact syxlabs.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to contact syxlabs.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/contactus
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
    "companyName": "futuristic",
    "firstName": "john",
    "lastName": "doe",
    "country": "nigeria",
    "phoneNo": "07012345789",
    "workEmail": "johndoe@gmail.com",
    "service": "nft",
    "moreInfo": "nft projects"
};
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="142">Parameter</th><th width="124">Parm Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>Contact Details</td><td>Body</td><td>Required</td><td>Contains information about the contact details. companyName, firstName, lastName, country, workEmail, service, and moreInfo is required. phoneNo and receiveInsights are optional.</td></tr></tbody></table>

#### Contact Us Object

Contains information about the new Contact details.

This object is used by the following operations:

* #### POST /v1/contactus

The properties included in the Contact details object are listed below.&#x20;

<table><thead><tr><th width="215">Property</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The contact detail unique ID. </td></tr><tr><td>companyName</td><td>string</td><td>The name of the company contacting syxlabs</td></tr><tr><td>firstName</td><td>string</td><td>The first name of the individual sending the contact details</td></tr><tr><td>lastName</td><td>string</td><td>The last name of the individual sending the contact details</td></tr><tr><td>country</td><td>string</td><td>The country the individual sendng the contact details resides in</td></tr><tr><td>phoneNo</td><td>string</td><td>The phone no. of the individual sendng the contact details </td></tr><tr><td>service</td><td>string</td><td>The service the individual needs syxlabs for.</td></tr><tr><td>moreInfo</td><td>string</td><td>More info about the service required</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the contact detail document was created.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the contact detail document was updated.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200 | 201, with information about the new waiting user.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Thur, 19 May 2023 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sa** <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "companyName": "futuristic",
        "firstName": "john",
        "lastName": "doe",
        "country": "nigeria",
        "phoneNo": "07012345789",
        "workEmail": "johndoe@gmail.com",
        "service": "nft",
        "moreInfo": "nft projects",
        "receiveInsights": false,
        "createdAt": "2023-05-19T15:52:58.538Z",
        "updatedAt": "2023-05-19T15:52:58.538Z",
        "id": "64679b5a4905bfe0438c2a64"
    }
}
```

#### &#x20;<a href="#top" id="top"></a>

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name            | Type            | Description                                     |
| --------------- | --------------- | ----------------------------------------------- |
| Contact Details | Contact Details | Contains information about  the Contact detail. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

