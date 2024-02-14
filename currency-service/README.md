# CURRENCY Service

The Currency service provides operations for managing currencies in the platform, such as adding, modifying, and deleting currencies and retrieving currency information.

| Action                            | EndPoint                            | Description                                                             |
| --------------------------------- | ----------------------------------- | ----------------------------------------------------------------------- |
| Create Currency                   | POST /v1/currencies                 | Allows the User to Create a new currency to the platform.               |
| Fetch Currencies                  | GET /v1/currencies                  | Allows the User to Fetch currencies on the platform.                    |
| Fetch Currency by Id              | GET /v1/currencies/:Id              | Allows the User to Fetch a currency by ID on the platform.              |
| Fetch Currency by Ticker          | GET /v1/currencies/ticker/:ticker   | Allows the User to Fetch a currency by ticker on the platform.          |
| Fetch Currency Network by ChainId | GET /v1/currencies/chainId/:chainID | Allows the User to Fetch a currency Network by chainId on the platform. |
| Update Currency                   | PUT /v1/currencies/:Id              | Allows the User to Update currency by ID on the platform.               |
| Delete Currency                   | DELETE /v1/currencies/:Id           | Allows the User to Delete currency by ID on the platform.               |
