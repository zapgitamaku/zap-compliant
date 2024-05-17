# Fetch Users LeaderBoard

### GET /v1/leaderBoard <a href="#top" id="top"></a>

Allows a user to get only the top 100 users on zap loyalty program leaderboard on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get the leaderboard

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/leaderBoard
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                   |
| ------------- | ------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                              |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login |

#### Leaderboard Object

Contains information about ZAP's platform Leaderboard.

<table><thead><tr><th width="240">Property</th><th width="150">Type</th><th>Description</th></tr></thead><tbody><tr><td>userId</td><td>string</td><td>The unique ID for a specific user.</td></tr><tr><td>referralPoints</td><td>number</td><td>The points from their referral fully verifying</td></tr><tr><td>transactionPoints</td><td>number</td><td>The points from every transaction</td></tr><tr><td>referralTransactionPoints</td><td>number</td><td>The points from their referrals each transaction</td></tr><tr><td>totalPoints</td><td>number</td><td>The total points accumulated.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the leaderboard.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 15 Apr 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": [
        {
            "userId": {
                "username": "gideondev"
            },
            "referralPoints": 0,
            "transactionPoints": 0,
            "referralTransactionPoints": 0,
            "totalPoints": 0,
            "createdAt": "2024-05-13T13:33:03.924Z",
            "updatedAt": "2024-05-13T13:33:03.924Z",
            "id": "6642168f80917bc5c209a46a"
        }
    ]
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name                  | Type                  | Description                                             |
| --------------------- | --------------------- | ------------------------------------------------------- |
| <h4>Leaderboard </h4> | <h4>Leaderboard </h4> | Contains information about leaderboard on ZAP platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
