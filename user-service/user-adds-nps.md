# User Adds NPS

### POST /v1/nps <a href="#top" id="top"></a>

Allows the zap user and guest to create an NPS about the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request for a zap user and guest to create an NPS

#### **Sample request** URL <a href="#top" id="top"></a>

```json
https://{hostname}/v1/nps
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
'guest-id': 650c491a92b406cbccd65f0e // only send if is guest using the endpoint
```

#### **Sample** Request Body <a href="#top" id="top"></a>

```json
{
    "userId": "6515a38ef6d2985656496941",
    "score": 8,
    "comment": "nice swapping",
    "isGuest": true // only send if is guest using the endpoint
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="241">Header</th><th>Description</th></tr></thead><tbody><tr><td>Content-type</td><td>application/json</td></tr><tr><td>Authorization</td><td>This is the ZAP API Platform authorization token, and must be sent with every API request that requires login.</td></tr></tbody></table>

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="105">Parameter</th><th width="108">Param Type</th><th width="97">Data Type</th><th width="102">Required</th><th>Description</th></tr></thead><tbody><tr><td>NPS</td><td>Body</td><td>Object</td><td>Required</td><td>Contains information about the nps data. userId and score are always required. Comment is optional. And for the Guest users pass a isGuest in body and guest-id header</td></tr></tbody></table>

#### NPS Object

Contains information about NPS data taken.

The properties included in the **NPS** object are listed below.&#x20;

| Property | Type   | Description                                       |
| -------- | ------ | ------------------------------------------------- |
| userId   | string | The userId of the either the login user or guest. |
| score    | number | The score of the nps. in between 0 and 10         |
| comment  | string | The comment  of the nps                           |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with a created nps object.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 12 Oct 2023 16:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "userId": "6515a38ef6d2985656496941",
        "onModel": "User",
        "comment": "nice swapping",
        "score": 8,
        "isGuest": false,
        "createdAt": "2023-10-12T16:52:26.011Z",
        "updatedAt": "2023-10-12T16:52:26.011Z",
        "id": "6528244aef9a866044848cff"
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name     | Type   | Description                                  |
| -------- | ------ | -------------------------------------------- |
| userData | Object | Contains information about ZAP platform nps. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured while processing the request                                                                                                                                                                                                                                                                                     |

