---
description: This section defines how to obtain API keys
---

# API Keys

#### POST /v1/login&#x20;

Initiates the login process by verifying the credentials of a user who is attempting to log in to the platform. It logs the user in, returning an authentication cookie that is used to make authenticated calls to the platform. The cookie is valid for 1 day.

### Sample Request&#x20;

The example below sends the email and password for authentication of the user logging in.

**Sample request URL**

```
https://{hostname}/v1/login
```

**Sample request headers**

```
'Content-Type: application/json'
```

**Sample request body**

```
{
     "email": "myemailaddress@myemail.com",
    "password": "P@ssw0rd"
}
```

**Sample request: Curl**

```markup
curl --location --request POST 'https://{hostname}/v1/login' \
-H 'Content-Type: application/json' \
--data '{
     "email": "myemailaddress@myemail.com",
    "password": "P@ssw0rd"
}'
```

### Request Headers&#x20;

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

### Request Parameters&#x20;

<table><thead><tr><th width="237">Parameter</th><th>Parm Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>LoginRequest</td><td>Body</td><td>LoginRequest</td><td>Required</td><td>Email and password for the user logging in. Both values are required.</td></tr></tbody></table>

#### LoginRequest Object

Includes information about a user logging in to the platform, for verification purposes.

This object is used by the following operations:

* #### POST /v1/login&#x20;

The properties included in the **LoginRequest** object are listed below. All properties are **required** in the request message.

| Property | Type   | Description                          |
| -------- | ------ | ------------------------------------ |
| email    | string | The user's registered email address. |
| password | string | The password set up by the user.     |

### Response

If successful, this operation returns HTTP status code 200, with an updated cookie for the user in JSON format.

### Sample Response

The sample response below shows the user logging in.

### Sample Response Headers

```
{
    "success": true,
    "data": {
        "name": "ZAP Africa",
        "email": "myemailaddress@myemail.com",
        "createdAt": "2023-01-24T19:14:19.582Z",
        "updatedAt": "2023-01-24T19:14:19.582Z",
        "id": "63d02e0bc8c116c1308d39fe",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI0IkpXVCJ9.eyJ1c2VyIjd7Im5hbWUiOiJoZWxzZHNsbyIsImVtYWlsIjoiaHVoc2lAZGtzMml3d3NkLmNvbSIsImNyZWF0ZWRBdCI6IjIwMjMtMDEtMjRUMTk6MTQ6MTkuNTgyWiIsInVwZGF0ZWRBdCI6IjIwMjMtMDEtMjRUMTk6MTQ6MTkuNTgyWiIsImlkIjoiNjNkMDJlMGJjOGMxMTZjMTMwOGQ1OWZlIn0sImlhdCI6MTY3NDY5MTcxMSwiZXhwIjoxNjc0Nzc4MTExfQ.WGnGojIgQLBY3ZsRdF26jazSJPb1csyBkDceAQ7GHvk"
    }
}
```

### Sample Response Body

```
// Some code
```

### Response Headers

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |
|              |                  |
|              |                  |

### Response Body

| Name          | Type          | Description                                              |
| ------------- | ------------- | -------------------------------------------------------- |
| LoginResponse | LoginResponse | Contains information returned as a result of logging in. |

### LoginResponse Object

Contains information returned as a result of logging in.

| Property  | Type     | Description                                                                                                      |
| --------- | -------- | ---------------------------------------------------------------------------------------------------------------- |
| name      | string   | By default this is FirstnameLastname                                                                             |
| email     | string   | The user's registered email address.                                                                             |
| id        | string   | The unique ID for a specific user.                                                                               |
| token     | string   | The authToken for the user, indicating that the user's credentials have passed validation. Also the bearer token |
| createdAt | dateTime | This property displays when the user account was created. Used only in response messages.                        |
| updatedAt | dateTime | This property displays when the user account was last updated. Used only in response messages.                   |

### Error Codes/Messages

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |

