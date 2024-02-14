# BANK Service

The Bank service provides operations for managing Banks in the platform, such as adding, modifying, and deleting banks and retrieving bank information.

<table><thead><tr><th>Action</th><th width="222.33333333333331">EndPoint</th><th>Description</th></tr></thead><tbody><tr><td>Add Bank</td><td>POST /api/v1/banks</td><td>Allows the Admin to Add a new bank to the platform.</td></tr><tr><td>Fetch Banks</td><td>GET /api/v1/banks</td><td>Allows the Admin to Fetch Banks on the platform.</td></tr><tr><td>Fetch Bank by Id</td><td>GET /api/v1/banks/:Id</td><td>Allows the Admin to Fetch Banks by ID on the platform.</td></tr><tr><td>Edit Bank</td><td>PUT /api/v1/banks/:Id</td><td>Allows the Admin to Modify Banks by ID on the platform.</td></tr><tr><td>Delete Bank</td><td>DELETE /api/v1/banks/:Id</td><td>Allows the Admin to Delete(soft) Banks by ID on the platform.</td></tr></tbody></table>
