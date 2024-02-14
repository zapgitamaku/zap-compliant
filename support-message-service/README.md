# Support Message Service

The Support Message service provides operations for managing Support Messages in the platform, such as adding, modifying, and deleting messages and retrieving support messages information.

| Action                                  | EndPoint                                 | Description                                                                                                  |
| --------------------------------------- | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| Create Support Message                  | POST /v1/support/messages                | Allows the User to Create a new support message in a conversation on the platform.                           |
| Create Support User Response  Message   | POST /v1/support/response/messages       | Allows the Support User to respond to a support message in a conversation on the platform.                   |
| Fetch Support Message by conversationId | GET /v1/support/:conversationId/messages | Allows the User to fetch all support messages in a specific conversation by conversationId  on the platform. |
| Fetch Support Message by Id             | GET /v1/support/messages/:id             | Allows the User to Fetch a support message by ID on the platform.                                            |
| Update Support Message                  | PUT /v1/support/messages/:id             | Allows the User to modify a support message by ID on the platform.                                           |
| Delete Support Message (soft)           | DELETE /v1/support/messages/:id          | Allows the User to Delete a support message by ID on the platform.                                           |
