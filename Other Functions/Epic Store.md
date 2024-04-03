---
order: 2000
---

!!!danger Important Notice
- You need to have the Self-Publishing Rights to use Epic Store Functions like Currency etc. (This costs about $100)
- You cannot test these stuffs in the editor, you need to package the game and test it through the Epic Store Client

Rest everything is cool :D
!!!

### Managing Offers

Available offers are managed via the [Epic Games Dev Portal](https://dev.epicgames.com/en-us/). 

Once you have paid the $100 submission fee to self-publish, you can start creating offers.


### Getting Available Offers

Once you have created some offers in the dev portal, you can pull these offers into your game using `GetEIKOffers`. This function will return a list of Offers with the following information available for each:

### Blueprint Code

!!!
This example blueprint only returns the first offer found. You'll need to adjust your code to retrieve all of the offers by looping through the `Offers` array that is returned.
!!!

[!embed](https://blueprintue.com/render/u336_6n8/)

***The offers structure is structured like below:***

`Item ID` - The unique Item ID for this offer. Used when purchasing in-game.

`Item Name` - The name of the offering in the store.

`Item Description` - The description of the offering in the store.

`Expiration Date` - If applicable, the date this offer expires.

`Long Description` - A longer description of the offer in the store.

`Numeric Price` - The price of the offer in the store.

`Price Text` - The full price text of the offer in the store.

`Release Date` - The release date the offer will become available in the store.

`Regular Price` - The regular, non sale price of the offer in the store.

`Regular Price Text` - The full price text for the non sale price of the offer in the store.

### Listing Owned Items

To display a list of items owned by the current logged in user, you can call `GetEIKOwnedItems`. This function will return an array of receipts that the logged in user has. The receipt will display line items of items purchased.

!!!
This example blueprint only returns the first owned item found. You'll need to adjust your code to retrieve all of the owned items by looping through the `Owned Item Names` array that is returned.
!!!
[!embed](https://blueprintue.com/render/jvm4k0pz/)

### Purchasing Items

To purchase items in your in-game shop, you can use the call `PurchaseItem` and pass in the unique Item ID (obtained from `GetEIKOffers`). This function will return a receipt if successful, and return an error message if not successful.

!!!
This example blueprint uses a sample ItemID of 1. You'll need to adjust your code to use an actual ItemID that links to an offer in your store on the Epic Games Dev Portal.
You can obtain Offer IDs using `GetEIKOffers`.
!!!
[!embed](https://blueprintue.com/render/gqjnfde4/)
