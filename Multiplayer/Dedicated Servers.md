<!-- Add video tutorials back in once they are done -->
<!-- [!badge variant="danger" target="blank" size="xl" icon="video" text="Video Tutorial"](https://retype.com/) -->

Dedicated Server hosting is meant to be easy with EOS Integration Kit. In place of the default 7777 port that EOS uses to run dedicated servers, we have methods to use different ports because usually what happens is that a single machine can run multiple dedicated server but if we use *default* method, we can only use a single port or to be precise, a single session on a single server. But with EIK, **you can use multiple sessions on a single machine.**

Let's see the outline of how this process works. We will assume we have a VM (Virtual Machine) where we run our servers. So whenever we start the Server.exe, UE will check which port is free to start the server on, like the first server will start on Port `7777`, then the next one will start on Port `7778` and so on.  Now, when EOS is informed of this server, the Port Info is passed too, thus allowing EOS to pass the updated information to all clients and making the clients join the correct server.


## Configuration for Server

For game to allow connections to dedicated servers, you need to make the dedicated server use our game mode, namely `EIK_BaseGameMode`.

==- Artifact Settings

1. Go to [DevPortal](https://dev.epicgames.com/portal/en-US/), then select your organization and then go to your product page. On the product page, go to **Product Settings** and then **Clients** and lastly press on `Add New Client`.

![](/static/Screenshot_25.png)

2. Name `Client Name` something rememberable for Server like *ServerClient*, and then on `Client Policy`, select `Create New Client Policy` 

![](/static/Screenshot_26.png)

3. Name `Client Policy Name` something rememberable for Server Policy like *ServerPolicy*, and the `Client Policy Type` as *TrustedServer* and press on Save/Add New Client Policy.

![](/static/Screenshot_27.png)

4. Now select Server Policy on `Add New Client` section and press on Add New Client.

![](/static/Screenshot_28.png)

5. Now add the the Server Artifact to the EOS Integration Kit as was done for the client.
===

## Hosting Server 

The code in below code has a little bit of delay, so that the server has enough time to be ready to be able to host sessions. 
[!embed](https://blueprintue.com/render/zhxbzn03/)

---
---
## Joining Server

Same as joining [Matchmaking Sessions](/Getting-Started/Configuration/#defaultengineini)
