# Complete Onboard User (New flow)

### POST /v1/users/:userId/completeOnboarding <a href="#top" id="top"></a>

Allows the Site Admin to completely onboard a user to add the user's referrer code and username

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to complete onboarding a user on the platform

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/users/:userId/completeOnboarding
```

#### **Sample request headers** <a href="#top" id="top"></a>

```javascript
'Content-Type: application/json'
```

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "referralCode": "david",
    "username": "bigveezus",
    "channel": "discord"
}
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="108">Parameter</th><th width="162">Param Type</th><th>Data Type</th><th>Required</th><th>Description</th></tr></thead><tbody><tr><td>referralCode</td><td>string</td><td>string</td><td>optional</td><td>referralCode</td></tr><tr><td>username</td><td>string</td><td>string</td><td>required</td><td>username of the user</td></tr><tr><td>channel</td><td>string</td><td>string</td><td>optional</td><td>signup channel/medium</td></tr></tbody></table>

#### Onboarding Object

Contains information about ZAP's platform user.

This object is used by the following operations:

* **POST /api/v1/users/**:userId/completeOnboarding

The properties included in the **User** object are listed below. All properties are **required** in the request message.

| Property     | Type   | Description                                    |
| ------------ | ------ | ---------------------------------------------- |
| username     | string | The unique username picked by the user         |
| channel      | string | The channel where the user was invited from    |
| referralCode | string | the unique username of a referrer or affiliate |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 201, with information about the newly created user.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 201 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```
{
    "success": true,
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |



### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                                                                                                                                                                                                                                                                                                             |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad request: Returned if the client sends a malformed request; for example, invalid parameters or body content.For example, you might get this response if you did not specify the content-type for the request, specified an incorrect content-type, or did not have the correct information in the request body (POST content). |
| 500  | An error occured processing the request                                                                                                                                                                                                                                                                                           |
