# Fetch FAQ Articles

### GET /v1/faq <a href="#top" id="top"></a>

Allows a User to get FAQ Articles on the platform.

#### HTTP Method <a href="#top" id="top"></a>

GET

## Sample Request <a href="#samplerequest" id="samplerequest"></a>

The example below shows a request to get a list of FAQ Articles.

#### **Sample request** URL <a href="#top" id="top"></a>

```
https://{hostname}/v1/faq/?
```

#### **Sample request query** <a href="#top" id="top"></a>

<table><thead><tr><th width="225">Key</th><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>bodyLimit</td><td>1</td><td>Optional query parameter that specifies the number of FAQ Articles in the response body</td></tr><tr><td>pageLimit</td><td>3</td><td>Optional query parameter that paginates the list of FAQ Articles in the response body</td></tr><tr><td>startDate</td><td></td><td>Optional query parameter that adds a start date range to the list of FAQ Articles in the response body</td></tr><tr><td>endDate</td><td></td><td>Optional query parameter that adds a end date range to the list of FAQ Articles in the response body</td></tr></tbody></table>



#### &#x20;**Sample request headers** <a href="#top" id="top"></a>

```
'Content-Type: application/json'
```

## Request Header <a href="#samplerequest" id="samplerequest"></a>

| Header       | Description      |
| ------------ | ---------------- |
| Content-type | application/json |

#### FAQ Article Object

The properties included in the **FAQ Articles** object are listed below.

| Property  | Type     | Description                                                                                   |
| --------- | -------- | --------------------------------------------------------------------------------------------- |
| id        | string   | The faq article unique ID.                                                                    |
| question  | string   | The question the faq article is giving an  answer.                                            |
| answer    | string   | The faq article answer to the question.                                                       |
| category  | string   | The category the faq article questions and answer falls into.                                 |
| writtenBy | string   | The ID of the faq article writer (site admin)                                                 |
| createdAt | dateTime | This property displays when the faq article was created. Used only in response messages.      |
| updatedAt | dateTime | This property displays when the faq article was last updated. Used only in response messages. |

## Response <a href="#samplerequest" id="samplerequest"></a>

If successful, this operation returns HTTP status code 200, with information about the FAQ Articles.

### Sample Response <a href="#samplerequest" id="samplerequest"></a>

The sample responses below shows successful completion of this operation.

#### **Sample** Response Header <a href="#top" id="top"></a>

```
HTTP/1.1 200 OK
Date: Tue, 25 Apr 2023 14:14:31 GMT
Content-Type: application/json; charset=utf-8
```

#### **Sample** Response Body <a href="#top" id="top"></a>

```json
 {
      success: true,
      data: {
        faqArticles: [ 
            {
            question: 'What is cryptocurrency?',
            answer: 'Cryptocurrency is a digital or virtual currency that uses cryptography for security and operates independently of a central bank.',
            category: 'Getting-Started',
            writtenBy: '6447cf7dba168c3452717b54',
            createdAt: '2023-04-25T13:02:58.350Z',
            updatedAt: '2023-04-25T13:02:58.350Z',
            id: '6447cf82ba168c3452717b5b'
          },
        ],
        bodyLimit: 10,
        pageLimit: 1,
        dataCount: 1
      }
    }
```

### Response Headers <a href="#samplerequest" id="samplerequest"></a>

| Headers      | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

### Response Body <a href="#samplerequest" id="samplerequest"></a>

| Name        | Type        | Description                                                |
| ----------- | ----------- | ---------------------------------------------------------- |
| FAQ Article | FAQ Article | Contains information about  FAQ Articles on ZAP  platform. |

### Error Codes <a href="#samplerequest" id="samplerequest"></a>

If the call is unsuccessful an error code/message is returned. One or more examples of possible errors for this operation are shown below.

| Item | Value                                   |
| ---- | --------------------------------------- |
| 404  | The resource could not be found.        |
| 500  | An error occured processing the request |

