# BANK Detail Service

The Bank Detail service provides operations for managing Bank details in the platform, such as adding, modifying, and deleting bank details and retrieving bank information.

| Action                         | EndPoint                          | Description                                                      |
| ------------------------------ | --------------------------------- | ---------------------------------------------------------------- |
| Create Bank Details            | POST /v1/bankdetails              | Allows the User to Create a new bank detail on the platform.     |
| Fetch Bank Details             | GET /v1/bankdetails               | Allows the Admin to Fetch bank details on the platform.          |
| Fetch Bank Details by Id\*     | GET /v1/bankdetails/:Id           | Allows the User to Fetch bank detail by ID on the platform.      |
| Fetch Bank Details by UserId\* | GET /v1/bankdetails/users/:userId | Allows the User to Fetch bank details by UserID on the platform. |
| Update Bank Details            | PUT /v1/bankdetails/:Id           | Allows the User to Update bank detail by ID on the platform.     |
| Delete Bank Details            | DELETE /v1/bankdetails/:Id        | Allows the User to Update bank detail by ID on the platform.     |
