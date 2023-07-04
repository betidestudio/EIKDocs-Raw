---
order: 1000
---
[!badge variant="danger" target="blank" size="xl" icon="video" text="Video Tutorial"](https://youtu.be/98ZtDQd6GSo)

So, now that you have the plugin installed, let's get started with configuration of the plugin so that you can test the game as soon as possible xD.

### Plugin Settings

Go to **Project Settings** and then go to *Game* -> *EOS Integration Kit*

![](/static/Screenshot_12.png)

Now, go to [Epic Games DevPortal](https://dev.epicgames.com/portal/en-US/) and create a new product or use existing product. 

### DefaultEngine.ini

Go to the Project Folder, then Config and open DefaultEngine.ini and set the following settings ->

```

[OnlineSubsystemEIK]
bEnabled=true

[OnlineSubsystem]
DefaultPlatformService=EIK

[/Script/OnlineSubsystemEIK.NetDriverEOS]
bIsUsingP2PSockets=true

[/Script/Engine.GameEngine]
!NetDriverDefinitions=ClearArray
+NetDriverDefinitions=(DefName="GameNetDriver",DriverClassName="OnlineSubsystemEIK.NetDriverEOS",DriverClassNameFallback="OnlineSubsystemUtils.IpNetDriver")


```

!!!
Dedicated servers require a different net driver configuration, please see [Multiplayer -> Dedicated Servers](</Multiplayer/Dedicated Servers.md>).
!!!

### Android/Oculus Quest Setup