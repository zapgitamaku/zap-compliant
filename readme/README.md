---
description: Detailed therein are the endpoints required for a seamless onboarding flow.
---

# Onboarding

The Onboarding service provides operations for managing users in the platform, such as adding, modifying, and deleting users and retrieving user information.

| Action                         | EndPoint                                   | Description                                                                  |
| ------------------------------ | ------------------------------------------ | ---------------------------------------------------------------------------- |
| Create Business User           | POST /v1/signup                            | Allows the Site Admin to create a new business user on the platform.         |
| Fetch Business User by Id      | GET /v1/business/:id                       | Allows the Site Admin to retrieve a business user's details on the platform. |
| Login Business User            | POST /v1/business/login                    | Allows the Site Admin to log in a user to the platform.                      |
| Invite Business Owner          | POST /v1/owner/invite                      | Allows the SIte Admin to invite a business owner.                            |
| ​Update Business Owner Details | ​                                          | ​                                                                            |
| Upload Business Documents      | <h3 id="top">POST /v1/business/upload</h3> |                                                                              |
|  Verify Business TN            |                                            |                                                                              |
| Business Owner Verification    |                                            |                                                                              |
