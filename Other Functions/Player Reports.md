# Reports

## Send Report

The function used to send the report is not complicated, in fact it is fairly easy. You need the target player's product user id, and the local players product user id. Then you simply let the player filing the report fill out the rest in some ui and press send report, calling the function with the player inputed parameters. 

!!!
There are a plenty of ways to get the target players product user id, one way is to simply store it in each player's player state and retrieve it that way. You can also retrive your friends product user id's by using get friends list.

!!!
- `Report Category` - The category for this report.
- `Report Message` - Optional message regarding the report.
- `Local PUID` - The local player's product user id (PUID), retrieved by using the "Get Product User Id" function.
- `Target PUID` - The target player's product user id (PUID), retrieved from the player state as mentioned above there is more ways to do this.

[!embed](https://blueprintue.com/render/f4ytvwhg/)


