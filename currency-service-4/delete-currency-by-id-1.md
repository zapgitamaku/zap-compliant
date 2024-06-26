# Fetch Specific User Rank

### Get /v1/leaderBoard/rank/:userId <a href="#top" id="top"></a>

Allows a site to get a specific user leaderboard rank on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch specific user rank on leaderboard

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/leaderBoard/rank/:userId
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

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with user leaderboard rank.

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
    "data": {
        "userRank": {
            "userId": "6515a38ef6d2985656496941",
            "totalPoints": 300,
            "referralPoints": 300,
            "transactionPoints": 0,
            "referralTransactionPoints": 0,
            "rank": 1,
            "avatar": "https://res.cloudinary.com/dclh3qo14/image/upload/v1716284948/avatar_10_1_gmil8i.png",
            "avatarBgColor": "#4E0BCF",
            "streak": 0,
            "multiplier": 1,
            "leaderboardId": "667b729f555588230fd76f59"
        },
        "total": 1
    }
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
