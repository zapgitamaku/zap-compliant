# Fetch FAQ Article by Id

### GET /v1/faq/:Id <a href="#top" id="top"></a>

Allows a User to fetch a FAQ Article by Id on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get a FAQ Article by ID.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/faq/:Id
```

#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

## Request Parameters <a href="#samplerequest" id="samplerequest"></a>

| Key | Value  | Description                                |
| --- | ------ | ------------------------------------------ |
| Id  | \<Id>  | The unique ID for a specific FAQ Article.  |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the FAQ Article.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Tue, 25 Apr 2023 13:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
{
      success: true,
      data: {
        "question": "What can I do with Zap ?",
        "answer": "Zap allows you exchange supported currencies or fiat from anywhere in Africa.. You can also use Zap to receive international payments easily. We currently only support swaps to Nigerian Naira.",
        category: 'Getting-Started',
        writtenBy: '6447d71e8652bcda5e9f6a99',
        createdAt: '2023-04-25T13:35:30.767Z',
        updatedAt: '2023-04-25T13:35:30.767Z',
        id: '6447d7228652bcda5e9f6aa0'
      }
  }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name        | Type        | Description                                                          |
| ----------- | ----------- | -------------------------------------------------------------------- |
| FAQ Article | FAQ Article | Contains information about  a specific FAQ Article on ZAP  platform. |

#### FAQ Article Object

The properties included in the **FAQ Article** object are listed below.

<table><thead><tr><th width="250.33333333333331">Property</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>The faq article unique ID. </td></tr><tr><td>question</td><td>string</td><td>The question the faq article is giving an  answer.</td></tr><tr><td>answer</td><td>string</td><td>The faq article answer to the question.</td></tr><tr><td>category</td><td>string</td><td>The category the faq article questions and answer falls into.</td></tr><tr><td>writtenBy</td><td>string</td><td>The ID of the faq article writer (site admin)</td></tr><tr><td>createdAt</td><td>dateTime</td><td>This property displays when the faq article was created. Used only in response messages.</td></tr><tr><td>updatedAt</td><td>dateTime</td><td>This property displays when the faq article was last updated. Used only in response messages.</td></tr></tbody></table>

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

