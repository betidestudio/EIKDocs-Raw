---
order: 2300
---
!!!DANGER Very Important
All statistics name should only be `Uppercase` letters. Do not use lowercase letters or spaces.
!!!
### Creating a new Player Statistic

Statistics are created on the Epic Devportal under the **Statistics** tab which is under **Progression** tab. You can create a new statistic by clicking the **Create Statistic** button. 

![](/static/Screenshot_32.png)

Now for creating the statistic, you need to fill the following details:

[!badge Name]: The name of the statistic. This is the name that will be used in the code. This should be in `UPPERCASE` letters only.

[!badge Aggregation Type]: The aggregation type of the statistic. This is the type of aggregation that will be used for the statistic. The aggregation types are:

- `Sum`: The sum of all the values of the statistic.
- `Latest`: The latest value of the statistic.
- `Max`: The maximum value of the statistic.
- `Min`: The minimum value of the statistic.

![](/static/Screenshot_33.png)

Now just press Create and you are done.

### Setting the Statistic in Code

Now that you have created the statistic, you need to set the statistic in the code. For this, you need to use the `Set EIK Stats` function. This function is used to set the statistic value for the player. The function takes in the following parameters:


[!badge Stat Name]: The name of the statistic that you want to set which you set on the DevPortal. This should be in `UPPERCASE` letters only.

[!badge Value]: The value of the statistic that you want to set. This value would be sent to EOS and the action will be taken depending on the Aggregation Type. 

[!embed](https://blueprintue.com/render/1i5d59hn/)

### Getting the Statistic in Code

Now that you have set the statistic, you need to get the statistic in the code. For this, you need to use the `Get EIK Stats` function. This function is used to get the statistic value for the player. The function takes in the following parameters:


[!badge Stat Name]: The array of names of the statistic that you want to get which you set on the DevPortal. These should be in `UPPERCASE` letters only.

[!embed](https://blueprintue.com/render/d3ige95f/)