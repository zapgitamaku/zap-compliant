---
description: Detailed therein are the endpoints required for a seamless onboarding flow.
---

# Onboarding

The Onboarding service provides operations for managing users in the platform, such as adding, modifying, and deleting users and retrieving user information.

<table data-header-hidden><thead><tr><th></th><th width="207"></th><th></th></tr></thead><tbody><tr><td>Action</td><td>EndPoint</td><td>Description</td></tr><tr><td>Create Business User</td><td>POST /v1/signup</td><td>Allows the Site Admin to create a new business user on the platform.</td></tr><tr><td>Fetch Business User by Id</td><td>GET /v1/business/:id</td><td>Allows the Site Admin to retrieve a business user's details on the platform.</td></tr><tr><td>Login Business User</td><td>POST /v1/business/login</td><td>Allows the Site Admin to log in a user to the platform.</td></tr><tr><td>Invite Business Owner</td><td>POST /v1/owner/invite</td><td>Allows the SIte Admin to invite a business owner.</td></tr><tr><td>Upload Business Documents</td><td>​POST /v1/business/upload</td><td>​Allows the Site Admin to upload single documents</td></tr><tr><td> Verify Business TN</td><td>PUT /v1/verifications/details</td><td>Allows the business user to verify TIN</td></tr></tbody></table>
