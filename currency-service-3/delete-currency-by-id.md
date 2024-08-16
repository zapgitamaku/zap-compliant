# Update Token Watchlist

### PUT /v1/preferences/watchlist <a href="#top" id="top"></a>

Allows a zap User to update their watchlist preference settings on the platform.

#### HTTP Method <a href="#top" id="top"></a>

PUT

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to update a user watchlist preference

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/preferences/watchlist
```

#### **Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
'Authorization: Bearer  <Bearer Token>'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header        | Description                                                                                                    |
| ------------- | -------------------------------------------------------------------------------------------------------------- |
| Content-type  | application/json                                                                                               |
| Authorization | This is the ZAP API Platform authorization token, and must be sent with every API request that requires login. |

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "userId": "6515a38ef6d2985656496941",
    "allowTokenWatchList": true,
    "tokensToAdd": ["6686c13708a2b18bb2acbd58"], //for adding new tokens to watchlist
     "tokensToRemove": ["6686c13708a2b18bb2acbd58"], //for removing tokens from watchlist
    "watchListPercentageChange": 2
}
```

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="178">Parameter</th><th width="98">Parm Type</th><th width="116">Required</th><th>Description</th></tr></thead><tbody><tr><td>Watchlist</td><td>Body</td><td>Required</td><td>Contains information about user watchlist preference on ZAP platform. userId is required, and the rest are optional.</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, sucess information.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 15 Aug 2024 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": "User Preference updated successfully"
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
