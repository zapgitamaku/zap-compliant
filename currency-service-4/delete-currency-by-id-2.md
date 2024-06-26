# Fetch Specific User Network

### Get /v1/leaderBoard/:userId/network <a href="#top" id="top"></a>

Allows a site to get a specific user leaderboard network on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to fetch specific user network

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/leaderBoard/:userId/network
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

If successful, this operation returns HTTP status code 200, with user leaderboard network.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 15 May 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": {
        "referrer": {
            "_id": "65689f8ce9f8611059ba3c3c",
            "username": "azeez",
            "rank": 3,
            "referrerLeaderboard": {
                "_id": "664b55300b80c306e764f906",
                "userId": "65689f8ce9f8611059ba3c3c",
                "referralPoints": 0,
                "transactionPoints": 0,
                "referralTransactionPoints": 0,
                "totalPoints": 12,
                "streak": 0,
                "multiplier": 1,
                "leaderboardId": "667b729f555588230fd76f59"
                "createdAt": "2024-05-13T13:33:03.924Z",
                "updatedAt": "2024-05-13T13:33:03.924Z",
                "__v": 0
            }
        },
        "referredUsers": [
            {
                "referredUserId": "647dea2605647ed1d5193b0a",
                "username": "david",
                "referredLeaderboard": [
                    {
                        "_id": "664b4bee0b80c306e764f903",
                        "userId": "647dea2605647ed1d5193b0a",
                        "referralPoints": 0,
                        "transactionPoints": 0,
                        "referralTransactionPoints": 0,
                        "totalPoints": 22,
                        "streak": 0,
                        "multiplier": 1,
                        "leaderboardId": "667b729f555588230fd76f59"
                        "createdAt": "2024-05-13T13:33:03.924Z",
                        "updatedAt": "2024-05-13T13:33:03.924Z",
                        "__v": 0
                    }
                ],
                "rank": 2
            }
        ]
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
