# Send Push Notifications

### POST /v1/notification/push <a href="#top" id="top"></a>

Allows an admin User to send a push notification to a single useror all users on the platform.

#### HTTP Method <a href="#top" id="top"></a>

POST

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to send push notifications.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/notification/push
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

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

#### **Sample request body** <a href="#top" id="top"></a>

```json
{
    "title":"Test Notiification",
    "body":"This is a test Notification",
    "data": {
        "buttonText": "Click Here", 
        "buttonAction": "https://zap.africa", 
        "image":""},
    "isBulk": true,
    "userId": "655ca834498fd72ce6d2d13c"

}
```

## Request Body <a href="#samplerequest" id="samplerequest"></a>

<table><thead><tr><th width="142">Parameter</th><th width="124">Parm Type</th><th width="101">Required</th><th>Description</th></tr></thead><tbody><tr><td>title</td><td>string</td><td>Required</td><td>This is the title of the notification</td></tr><tr><td>body</td><td>string</td><td>Required</td><td>This is the body of the notification</td></tr><tr><td>data</td><td>object</td><td>Required</td><td>This contains the buttonText and buttonAction fields</td></tr><tr><td>isBulk</td><td>boolean</td><td>Required</td><td>this is either true or false</td></tr><tr><td>userId</td><td>string</td><td>optional</td><td>this is optional, but required when isBulk is false</td></tr></tbody></table>

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the notifications.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Wed, 25 Jan 2023 23:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
    "success": true,
    "data": "Push notification sent successfully"
}
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description                    |
| ------------ | ------------------------------ |
| Content-Type | application/json charset=utf-8 |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name             | Type  | Description                                                  |
| ---------------- | ----- | ------------------------------------------------------------ |
| NotificationData | array | Contains objects containing information about notifications. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |
