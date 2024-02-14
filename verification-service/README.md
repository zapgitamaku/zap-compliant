# VERIFICATION Service

The Verification service provides operations for managing User verification in the platform, such as adding, modifying, deleting and retrieving Verification information.

| Action                                 | EndPoint                       | Description                                                                          |
| -------------------------------------- | ------------------------------ | ------------------------------------------------------------------------------------ |
| Create Verification                    | POST /v1/verifications         | Allows the User to Create a new user verification Document on the platform.          |
| Fetch Verifications                    | GET /v1/verifications          | Allows the User to Fetch user verification data on the platform.                     |
| Fetch Verification by Verification Id  | GET /v1/verifications/:Id      | Allows the User to Fetch  User Verification data by Verification ID on the platform. |
| Fetch Verification by User Id          | GET /v1/verifications/user/:id | Allows the User to Fetch  User Verfication data by User ID on the platform.          |
| Update Verfication by Verification Id  | PUT /v1/verifications/:Id      | Allows the User to Update User Verification data by Verification ID on the platform. |
| Update Verfication by User Id          | PUT /v1/verifications/user/:id | Allows the User to Update user Verification data by User ID on the platform.         |
| Delete Verification by Verification Id | DELETE /v1/verifications/:Id   | Allows the User to Delete User Verification data by verification ID on the platform. |
