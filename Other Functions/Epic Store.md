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

`ItemID` - The unique Item ID for this offer. Used when purchasing in-game.

`ItemName` - The name of the offering in the store.

`ItemDescription` - The description of the offering in the store.

`ExpirationDate` - If applicable, the date this offer expires.

`LongDescription` - A longer description of the offer in the store.

`NumericPrice` - The price of the offer in the store.

`PriceText` - The full price text of the offer in the store.

`ReleaseDate` - The release date the offer will become available in the store.

`RegularPrice` - The regular, non sale price of the offer in the store.

`RegularPriceText` - The full price text for the non sale price of the offer in the store.

### Listing Owned Items

To display a list of items owned by the current logged in user, you can call `GetEIKOwnedItems`. This function will return an array of receipts that the logged in user has. The receipt will display line items of items purchased.

### Purchasing Items

To purchase items in your in-game shop, you can use the call `PurchaseItem` and pass in the unique Item ID (obtained from `GetOffers`). This function will return a receipt if successful, and return an error message if not successful.
