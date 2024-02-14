# FAQ Article Service

The FAQ Article service provides operations for managing FAQ Articles in the platform, such as adding, modifying, and deleting FAQ Articles and retrieving articles information.

| Action                         | EndPoint                       | Description                                                               |
| ------------------------------ | ------------------------------ | ------------------------------------------------------------------------- |
| Create FAQ Articles            | POST /v1/faq                   | Allows the site admin user to Create a new FAQ Article on the platform.   |
| Fetch FAQ Articles             | GET /v1/faq                    | Allows the User to Fetch FAQ Articles on the platform.                    |
| Fetch  FAQ Articles by Id      | GET /v1/faq/:Id                | Allows the User to Fetch a FAQ Article by ID on the platform.             |
| Fetch FAQ Articles by category | GET /v1/faq/category/:category | Allows the User to Fetch FAQ Articles by category on the platform.        |
| Update FAQ Articles            | PUT /v1/faq/:id                | Allows the site admin user to Modify a FAQ Article by ID on the platform. |
| Delete FAQ Articles (soft)     | DELETE /v1/faq/:id             | Allows the site admin user to Delete a FAQ Article by ID on the platform. |
