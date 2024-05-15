# User Information

!!!info At the end of the page there is documentation for structures and enumerations

## Find Player By Display Name

!!!warning Find player by display name only works for Epic Accounts

Players are not expected to know their friends user id, only their display name. Use this function yo find a player from an inputed display name.

#### Find Player By Display Name Input Parameters

`Target Display Name` The target players display name

`Local Epic Account Id` The epic account id for the local player

#### Find Player By Display Name Return Values

`EIK User Info` A struct containing information about the user

---

## Get External Accounts From Product User Ids

This funcion gets all external account mappings from an array of product user ids. 

### Get External Accounts From Product User Ids Input Parameters

`Target Product User Ids` An array of product user ids that you want to retrive external account mappings for

`Local Product User Id` The product user id of the player making the request 

### Get External Accounts From Product User Ids Return Values

`ProductUserIdAndExternalAccountIds` An array of the struct *ExternalAccountIdAndType* containing each players external account information and a product user id. 

---

## Get Product User Id From External Account Id

Most game services in eos are product user id based, it is nice to be able to retrive a product user id from an external account, such as an Epic Id. 

### Get Product User Id From External Account Id Input Parameters

`AccountIds` An array of the struct *ExternalAccount* containing the user id and the account type.

`LocalProductUserId` The product user id of the player calling the function

### Get Product User Id From External Account Id Return Values

`ProductUserIdAndAccountId` An array of the struct ProductUserIdAndAccountId containing information about each product user id found

---

### Structures
---
`EIK User Info`

    String: Display Name
    String: Epic Account Id
    String: Country (Can be null)
    String: Nickname (Can be null)
    String: Preffered Language (Can be null)
---
`ExternalAccountIdAndType`

    Enum ExternalAccountTypes: External Account type
    String: Account Id
    String: Display Name
    DateTime: Last login
---
`ProductUserIdAndExternalAccountIds`

    (Array) Struct ExternalAccountIdAndType: ExternalAccountIds
    String: Product User Id
---
`ExternalAccount`

    String: Account Id
    Enum ExternalAccountTypes: The account type
---
`ProductUserIdAndAccountId`

    String: Account Id
    Enum ExternalAccountTypes: External Account type
    String: Product User Id


#### Enumerations
---
`ExternalAccountTypes`

    EOS_EAT_EPIC	
    EOS_EAT_STEAM
    EOS_EAT_PSN
    EOS_EAT_XBL
    EOS_EAT_DISCORD
    EOS_EAT_GOG
    EOS_EAT_NINTENDO
    EOS_EAT_UPLAY
    EOS_EAT_OPENID
    EOS_EAT_APPLE
    EOS_EAT_GOOGLE
    EOS_EAT_OCULUS
    EOS_EAT_ITCHIO
    EOS_EAT_AMAZON
---
