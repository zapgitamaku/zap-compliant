# Fetch All Waiting Users

### GET /v1/users <a href="#top" id="top"></a>

Allows the Admin user to fetch information about all the waiting users.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows an admin user request to get all waiting users.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/users
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                       |
| ------------- | ------------------------------------------------- |
| Content-type  | application/json                                  |
| Authorization | This is the ZAP Waitlist API authorization token. |

#### Waiting User Object

Contains information about the Waiting Users.

This object is used by the following operations:

* #### POST /v1/user
* #### GET /v1/users

The properties included in the waiting user object are listed below.&#x20;

<table><thead><tr><th>Property</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The user unique ID.  </td></tr><tr><td>email</td><td>string</td><td>The unique email of the waiting use.</td></tr><tr><td>emailSubmissionTime</td><td>dateTime</td><td>This field shows when the waiting user was added.</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the waiting user was created.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the waiting user was last updated.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the waiting users.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Thur, 10 May 2023 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
      "success": true,
      "data": [
          {
            "email": "sunlight@gmail.com",
            "emailSubmissionTime": "2023-05-11T10:26:53.128Z",
            "createdAt": "2023-05-11T10:52:33.039Z",
            "updatedAt": "2023-05-11T10:52:33.039Z",
            "id": "645cc2f832ebfe431d35f462"
          }
      ]
    }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name          | Type          | Description                                             |
| ------------- | ------------- | ------------------------------------------------------- |
| Waiting Users | Waiting Users | Contains information about ZAP  platform waiting users. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

