# Create New Waiting User

### POST /v1/user <a href="#top" id="top"></a>

Add a new waiting user email.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to Create a new waiting user.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/user
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

#### &#x20;**Sample request body** <a href="#top" id="top"></a>

```json
{
      "email": "sunlight@gmail.com",
};
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="142">Parameter</th><th width="124">Parm Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>User</td><td>Body</td><td>Required</td><td>Contains information the new waiting user. email is required.</td></tr></tbody></table>

#### Waiting User Object

Contains information about New Waiting User.

This object is used by the following operations:

* #### POST /v1/user
* #### GET /v1/users

The properties included in the Waiting User object are listed below.&#x20;

<table><thead><tr><th width="215">Property</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The user unique ID. </td></tr><tr><td>email</td><td>string</td><td>The unique email of the waiting user.</td></tr><tr><td>emailSubmissionTime</td><td>dateTime</td><td>This field shows when the waiting user was added.</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the waiting user was created.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the waiting user was last updated.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200 | 201, with information about the new waiting user.

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
      "data": {
        "email": "sunlight@gmail.com",
        "emailSubmissionTime": "2023-05-11T10:26:53.128Z",
        "createdAt": "2023-05-11T10:52:33.039Z",
        "updatedAt": "2023-05-11T10:52:33.039Z",
        "id": "645cc2f832ebfe431d35f462"
      }
    }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name | Type | Description                                   |
| ---- | ---- | --------------------------------------------- |
| User | User | Contains information about  the Waiting User. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

