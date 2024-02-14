# MARKET Service

The Market service provides operations for managing currencies in the platform, such as adding, modifying, and deleting currencies and retrieving currency information.

| Action             | EndPoint               | Description                                              |
| ------------------ | ---------------------- | -------------------------------------------------------- |
| Create Market      | POST /v1/markets       | Allows the User to Create a new market to the platform.  |
| Fetch Market       | GET /v1/markets        | Allows the User to Fetch markets on the platform.        |
| Fetch Market by Id | GET /v1/markets/:Id    | Allows the User to Fetch a market by ID on the platform. |
| Update Market      | PUT /v1/markets/:Id    | Allows the User to Update market by ID on the platform.  |
| Delete Market      | DELETE /v1/markets/:Id | Allows the User to Delete market by ID on the platform.  |
