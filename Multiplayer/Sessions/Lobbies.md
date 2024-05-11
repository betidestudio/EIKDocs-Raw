<!-- Add video tutorials back in once they are done -->
<!-- [!badge variant="danger" target="blank" size="xl" icon="video" text="Video Tutorial"](https://retype.com/) -->

## Creating a Lobby Session
Here, as in the code, call Create EIK Lobby. 


`Is Lan Boolean` - Set this to TRUE will make the game un-noticeable on the EOS DevPortal website. Expected to be false.

`Number Of Public Connection Integer` - Number of players who can join the session through matchmaking. Invites are not managed by this number.

`Number Of Private Connection Integer` - Number of players who can join the session through invitations or direct joining.

`Should Advertise Boolean` - If this is set to TRUE, then this session would come up on the Find Sessions node.

`Allow Join In Progress Boolean` - If this is set to TRUE, then the players will not be able to join session if the session has started.

`Use Voice Chat Boolean` - If this is set to TRUE, all players will automatically connect to voice chat.

`Region Enum` - This allows to select regions(one of it's kind matchmaking). If you make it No Selection, it will appear it in all cases normally.

`Custom Settings TMAP` - You may set custom settings like game mode etc.


[!embed](https://blueprintue.com/render/qhzb-vso/)

---
---

## Finding a Lobby Session
Here, as in the code, call Find EIK Sessions.

`Session Settings TMAP` - You may set custom settings like game mode etc.

`Match Type Enum` - Should be **Lobby** for finding Lobby Sessions.

`Region Enum` - This allows to select regions(one of it's kind matchmaking). If you make it No Selection, it will appear it in all cases normally.

[!embed](https://blueprintue.com/render/ovuuiswx/)

### Response of Find EIK Sessions

If the request is success, then the `Session Results Array` holds all the session it was able to find as per your searchn request and holds the details with additional information. Let's see what all info it has.

Now each Session Result Struct holds the following info ->

`Session Result` - Used to join the session.

`Session Settings` - Holds all the settings for the session that were set by you during the session creation process.

`Session Name` - The Session Name set on Session Creation Process

`Is Dedicated Server` - Not used for Lobby Sessions

---
---

## Joining a Lobby Session
Here, as in the code, call Join EIK Sessions.
!!!warning
In the blueprint code below, the loop will make the user to join all sessions found. Please correct it to make it join a single session.
!!!
`Session To Join` - This value is passed by the Find EIK Sessions node. 
[!embed](https://blueprintue.com/render/3lphx-dw/)

---
---