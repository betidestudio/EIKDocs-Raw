

!!!danger 
Steam ID 480 cannot be used anymore. You require to pay Steam Direct Fee to be able to use Steam Login
!!!

1. Go to [Dev Portal](https://dev.epicgames.com/portal/en-US/) and then to Product Settings of the product/game you are using. 

![](/static/image.png)

2. Go to Identity Providers, and press on Add Identity Provider

![](/static/spaces_rX4RNC7NdsMt2GSjBUkF_uploads_IbhDKBCxJgsIPCRwDYGy_image.png)

3. Set **Steam Networking Identity** and **Encryption Key** to be *empty*. Also, set the Steam ID to be same as your Steam ID

![](/static/image2.png)

4. Now go to Sandboxes and the press on Identity Providers and select Steam and Save

![](/static/Screenshot_15.png)

5. Headover to Unreal Engine, then Plugins and enable **Online Subsystem Steam**

![](/static/image4.png)

6. Configure the `DefaultEngine.ini` and add these lines

```
[OnlineSubsystemSteam]
bEnabled=true
SteamDevAppId=[Your Steam ID]
```

One more thing to configure is the `[OnlineSubsystem]` in the same file

```
[OnlineSubsystem]
DefaultPlatformService=EIK
NativePlatformService=Steam
```

7. Call this blueprint code to login using EIK

