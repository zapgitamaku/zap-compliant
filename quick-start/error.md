# Error

## Introduction

To indicate the success or failure of an API request, ZAP employs a standard HTTP response code. Code in the 2xx range indicates success and that things are working properly, whereas code in the 4xx range indicates that things are not going so well. This is mostly the fault of the client. These issues can range from unauthorized access to incorrect parameters being sent to resources that do not exist.

A status code in the 5xx range indicates problems on our end, such as when a service is not available and graceful exception handling is either impossible or not practical.



| Code | Error               | Status |
| ---- | ------------------- | ------ |
| 200  | Success             |        |
| 201  | Created             |        |
| 400  | BadRequest          |        |
| 401  | Unauthorised        |        |
| 403  | Forbidden           |        |
| 404  | NotFound            |        |
| 422  | Unprocessable       |        |
| 500  | InternalServerError |        |
