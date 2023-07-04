---
order: 2000
---
[!badge variant="danger" target="blank" size="xl" icon="video" text="Video Tutorial"](https://retype.com/)


Let's get started with installing EOS Integration Kit into your projects, which would be the easiest step, hopefully.

!!!danger 📢 Important Precaution
To ensure seamless integration with the EOS Integration Kit, it is recommended to deactivate the default EOS plugins bundled with the Unreal Engine to avoid any potential conflicts.
!!!  

### Marketplace Edition
[!button variant="primary" icon="download" iconAlign="left" text="Download Marketplace Edition"](https://www.unrealengine.com/marketplace/en-US/product/eos-integration-kit)

So firstly, if you are using the marketplace version, thanks for the purchase 🫡
If you have bought the plugin, go the Epic Launcher and follow the below steps ->
1. Open Library in the Unreal Engine Section of the Epic Launcher

![](/static/imagestep1plugininstallartion.png)

2. Check Valut and install the plugin for the version you want to use

![](/static/Screenshot_2.png)
![](/static/Screenshot_3.png)

3. Now open or create a project with the same Unreal Engine Version and go to the Plugins section.

![](/static/Screenshot_4.png)

4. Enable the Plugin and Restart the Editor

![](/static/Screenshot_5.png)

**Done, now you have the plugin ready and are ready to move to the next step 🤝**

### GitHub Edition
[!button variant="primary" icon="download" iconAlign="left" text="Download Github Edition"](https://github.com/betidestudio/EOSIntegrationKit/releases)

Github has two way to get the files, one is the Normal Clone/Download and second is the Release Section. We suggest that you use the Releases version of the plugin for which the link is linked above.
1. Go the Github Releases Section and download the latest version for the version you are using.

![](/static/Screenshot_6.png)

SidePoint - Please star the repo.

![](/static/Screenshot_7.png)

2. Create a C++ Project OR if you have a Blueprint Project already, then just add a empty C++ class and that will do the job.

![](/static/Screenshot_8.png)

3. Go to Project Explorer, then create a folder named Plugins and lastly paste the downloaded files in that folder.

![](/static/Screenshot_9.png)

![](/static/Screenshot_10.png)

4. Right click .uproject file and **Generate Visual Studio Files**

![](/static/Screenshot_11.png)

5. Now open the .uproject file and probably, it may ask if you want to rebuild, which you can let it to and done.