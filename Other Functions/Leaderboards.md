[!badge variant="danger" target="blank" size="xl" icon="video" text="Video Tutorial"](https://youtu.be/tCuE6YOg_-I?si=saGI9DT7IiF_DwjO)

### Create Global Leaderboard

Go to Leaderboards under Progression in Game Services and then press on Create Leaderboard

![Create Leaderboard](image-8.png)

You just need to put the Leaderboard Name, and connect a stat to the leaderboard. Now if you want a time-based leaderboard, then you can select End Time or else, just tick `Never Expire this leaderboard`.

![Leaderboard](image-9.png)


### Get Global Leaderboard 

You can get any global leaderboard by using the below function. It will return the leaderboard in a struct. You will notice it has a Range and Around Range input fields. Range is the number of entries you want to get from the leaderboard and Around Range is the number of entries you want to get around the player's rank.

So for example, if you want the first 200 entries from the leaderboard, then you can set Range to 100 and Around Range to 100. This will give you the entries from 0 to 200

[!embed](https://blueprintue.com/render/xzinfj9m/)

### Get Leaderboard For User Ids

You can create a unranked leaderboard for an array of player ids. The most common use case for this is to have a unranked leaderboard for your friends. You can use the read friendslist function to get all of your friends userids. 

The way this function works is it creates a leaderboard based on a stat. So you don't need to create a leaderboard in developer portal. 

The function will not return display names nor a rank. If the player does not have a score, they will not appear in the leaderboard. Those are limitations to eos and not eik. Please see the *Get External Accounts From Product User Ids* in the side *User Info* for more information on retriving display name from a product user id.

#### Unranked Leaderboard Parameters 
 `Local User Id` Your own product user id
 `Target User Ids` All the players you want to include in your leaderboard
 `Use Time` If you whish to set a timerange for the scores in the leaderboard
 `Start Time`
 `End Time` 
 `Aggregation Type` The aggregation type set for the stat in epic dev portal. (Sum, latest min or max)
 `Stat Name` The name of the stat
#### Unranked Leaderboard Return Values 
`Score` The users score
`User Id` The users product user id