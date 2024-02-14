# Support Conversation Service

The Support Conversation service provides operations for managing Support Conversations in the platform, such as adding, modifying, and deleting conversations and retrieving conversations  information.

| Action                                   | EndPoint                                | Description                                                                                                                           |
| ---------------------------------------- | --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Create Support Conversation              | POST /v1/support/conversations          | Allows the User to Create a new support conversation to the platform.                                                                 |
| Fetch Support Conversations by userId    | GET /v1/support/:userId/conversations   | Allows the User to Fetch all their support conversations on the platform.                                                             |
| Fetch Support Conversations by supportId | GET /v1/support/conversations/supportId | Allows the Support User to Fetch all their support conversations and conversations with no support user response yet on the platform. |
| Fetch Support Conversation by Id         | GET /v1/support/conversation/:id        | Allows the User to Fetch support conversation by ID on the platform.                                                                  |
| Close Support Conversation by Id         | GET /v1/support/conversation/:id/close  | Allows the User to close  support conversation by id on the platform.                                                                 |
| Update Support Conversation              | PUT /v1/support/conversation/:id        | Allows the User to modify support conversation by ID on the platform.                                                                 |
| Delete Support Conversation (soft)       | DELETE /v1/support/conversation/:id     | Allows the User to Delete support conversation by ID on the platform.                                                                 |
