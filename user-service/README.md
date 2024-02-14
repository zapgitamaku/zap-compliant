# USER Service

The Users service provides operations for managing users in the platform, such as adding, modifying, and deleting users and retrieving user information.

| Action               | EndPoint                | Description                                                                    |
| -------------------- | ----------------------- | ------------------------------------------------------------------------------ |
| Create user          | POST /v1/users          | Allows the Site Admin to create a new user on the platform.                    |
| Fetch users          | GET /v1/users           | Allows the Site Admin to retrieve a list of users on the platform.             |
| Fetch user by Id     | GET /v1/users/:id       | Allows the Site Admin to retrieve a particular user's details on the platform. |
| Edit user by Id      | PUT /v1/users/:id       | Allows the Site Admin to modify a particular user's details on the platform.   |
| Delete user by Id    | DELETE /v1/users/:id    | Allows the Site Admin to erase a particular user's details from the platform.  |
| Log in user          | POST /v1/login          | Allows the Site Admin to log in a user to the platform.                        |
| Change user password | POST /v1/changePassword | Allows the Site Admin to change a user's password on the platform.             |
| Reset user password  | POST /v1/forgotPassword | Allows the Site Admin to reset a user's password on the platform.              |

