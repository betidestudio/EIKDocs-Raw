<style>
    .sample {
        text-align: center;
        color: #1956AF;
        border-radius: 10px;
        background-color: #E1EDFF;
        border: 1px solid #1956AF;
        padding-top: 20px;
        margin-bottom: 20px;
    }
</style>


:::sample { #container1 }
This method is called `Obvious Method` because although EOS team states it as a trusted server login, most games would likely be more likely to use this method for Listen Servers too.
:::

So, what is Obvious Method? It is a method where the client sends the user credentials to the server and the server creates a token and sends it back to the client for them to conenct to the voice channel. This method is used for both Dedicated Servers and Listen Servers. The only difference is that in Dedicated Servers, the server is the one that verifies the credentials with the EOS backend, while in Listen Servers, the client is the one that verifies the credentials with the EOS backend.

### Code Setup
!!!light Just a small info...
This code doesn't require the players to require to login using EOS Methods. You can use voice chat functions with or without doing other EOS Login Setup.
!!!


`Voice Room Name` - The name of the voice room that you want to join. For instance, if you have a game similar to Pubg or Fortnite, where there are 100 players with teams of 4, then you can have 25 voice rooms with 4 players each. This will allow you to have a voice room for each team.

`Player Name` - The name of the player that you want to join the voice room with. This is the name that will be displayed in the voice room.

`Client IP` - The IP of the client. You can use **10.0.0.1** as the default value if you don't want to pass the IP. If you pass the IP, EOS will connect you to nearest available voice server.
[!embed](https://blueprintue.com/render/6kplwrq8/)


### Voice Functions