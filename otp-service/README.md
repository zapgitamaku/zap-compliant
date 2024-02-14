# OTP Service

The Users service provides operations for managing users in the platform, such as adding, modifying, and deleting users and retrieving user information.

| Action       | EndPoint            | Description                                                                              |
| ------------ | ------------------- | ---------------------------------------------------------------------------------------- |
| Generate OTP | POST /v1/otp/       | Allows the Site Admin to generate a Secure OTP for a new user on the platform.           |
| Verify OTP   | POST /v1/otp/verify | Allows the Site Admin to verify a user's secure OTP during an operation on the platform. |

