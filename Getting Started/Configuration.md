---
order: 1000
---
<!-- Add video tutorials back in once they are done -->
<!-- [!badge variant="danger" target="blank" size="xl" icon="video" text="Video Tutorial"](https://youtu.be/tCuE6YOg_-I?si=saGI9DT7IiF_DwjO) -->

So, now that you have the plugin installed, let's get started with configuration of the plugin so that you can test the game as soon as possible xD.

### Plugin Settings

Go to **Project Settings** and then go to *Game* -> *EOS Integration Kit*

![](/static/Screenshot_12.png)

Now, go to [Epic Games DevPortal](https://dev.epicgames.com/portal/en-US/) and create a new product or use existing product. Fill out the values in your project settings with the ones you got from eos dev portal. 

### Leave lobby button

For the leave lobby button in social overlay to work you need to specify a level name that the player should open. If you leave bland it will open your default game level.

### DefaultEngine.ini

!!!danger As of plugin version 2.5.0 this step is no longer required.
!!!
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
+NetDriverDefinitions=(DefName="GameNetDriver",DriverClassName="OnlineSubsystemEIK.NetDriverEIK",DriverClassNameFallback="OnlineSubsystemUtils.IpNetDriver")


```

!!!
Dedicated servers require a different net driver configuration, please see [Multiplayer -> Dedicated Servers](</Multiplayer/Dedicated Servers.md>).
!!!


### Android/Quest Setup

1. Go to Project Settings -> EIK Android/IOS Settings and set all the settings. You can get the Client ID and Client Secret from the Epic Games DevPortal.
2. Now go to your project folder and go to `Config/Android` and open `AndroidEngine.ini` and add the following settings ->

```
[OnlineSubsystemEIK]
bEnabled=true

[OnlineSubsystem]
DefaultPlatformService=EIK

[/Script/OnlineSubsystemEIK.NetDriverEIK]
bIsUsingP2PSockets=true

[/Script/Engine.GameEngine]
!NetDriverDefinitions=ClearArray
+NetDriverDefinitions=(DefName="GameNetDriver",DriverClassName="OnlineSubsystemEIK.NetDriverEIK",DriverClassNameFallback="OnlineSubsystemUtils.IpNetDriver")

``````

3. Done! Now you can package the game and test it on your device.