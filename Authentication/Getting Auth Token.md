# Retriving Auth Token

!!!warning This is only supported by Epic Accounts

### Get The Auth Token

The auth token can be requested and retrived at any moment after a successful login. Some use cases for this include open id authentication on services like playfab or your custom backend. 

### Get The Auth Token Inputs

`EpicId` The Epic Account Id of the logged in user, which will be used to get the auth token

### Get The Auth Token Return Values

`Epic Account Id` The Epic Account Id associated with the id token

`Id Token` The id token as a JTW (JSON Web Token) string