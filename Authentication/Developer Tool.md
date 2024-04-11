With this method, developers can use the Epic Developer Tool, which allows pre-authenticated accounts to be used for testing authentication in your game.


### Setting Up The Developer Tool

To get access to the Developer Tool, download the latest EOS SDK from the Epic Games dev portal. Once extracted, open the extracted folder and locate the `SDK/Tools` folder. Find the appropriate dev tool for your operating system. (darwin for Mac, win32 for Windows) and extract the contents.

Run `EOS_DevAuthTool` from the extracted folder. 

You will be presented with a screen like below:

![](/static/devtool_start.png)

Select which port you want the dev tool to run on (Default is 6300) and click `Start`

Afterward, you will be presented with the Devtool interface.

![](/static/devtool_interface.png)

Click the 'Login' button and you will be prompted with an Epic Games account login interface.

![](/static/devtool_login.png)

Once logged in, you will be asked to provide a name for this login. In this example, we use `Context_1`. 

![](/static/devtool_addcontext.png)

Add as many accounts as you need for testing. All of your added accounts will appear on the left side of the interface.

![](/static/devtool_contextlist.png)

### Blueprint Code

[!embed](https://blueprintue.com/render/v0qqrgva/)

When using the Developer Tool, the following pins are required:

`Login Method` - Select **Developer** from the list of enumerations.

`Display Name` - The URL and port to the developer portal application. This can be found in the developer portal interface in the to left corner. In our example, it is **localhost:6300**.

`Token` - This is one of the names for your logins provided by you when you created a login. This is case sensitive.

Upon using a developer portal login for the first time, you must go through the authentication approval process. Once you have completed this you will not need to do it again. 

In order to use multiple accounts (e.g. one per standalone editor window) during testing, it will require creating some widgets for determing which window logs into which account.