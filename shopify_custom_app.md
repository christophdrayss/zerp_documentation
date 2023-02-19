# How to create a Shopify custom app for zerp

Zerp needs a custom app to be connected to Shopify and perform several tasks:
1) Create a new order once someone purchased an item via Zalando
2) Synchronize the stock
3) Have infos about the products in order to match attributes and IDs with Zalando system.

## Step 1.

Go into your Shopify dashboard, in "Settings" and click "Apps and sales channels", then "Develop apps".

![image](https://user-images.githubusercontent.com/43708486/219960728-0517d533-6ffb-49f9-96ef-73033da593ae.png)

## Step 2.

Click "Create an app", enter an arbitrary name, such as "Zalando Syncing App" or similar, and create the app.

![image](https://user-images.githubusercontent.com/43708486/219960837-008a21b8-c84f-4ca3-9f1c-ff5bc841613c.png)

## Step 3.

You now have the app with a plain dashboard like this. Click "Configure Admin API scopes" to give access permissions.

![image](https://user-images.githubusercontent.com/43708486/219960976-b2be87c8-9f3b-4a54-bf91-a64482592374.png)

## Step 4.

Search the permissions for *Products*, *Orders* and *Inventory* and give the following permissions.

This allows zerp to read product information, read+write inventory amounts, and read+write orders (zerp does not need to read orders but writing always implies also reading).
Click "Save" thereafter.

![image](https://user-images.githubusercontent.com/43708486/219961188-afd69fc2-adca-4a63-8ee3-b715095ff8c8.png)
![image](https://user-images.githubusercontent.com/43708486/219961193-b10ea32f-f3ed-4680-81f3-8a27874c8984.png)
![image](https://user-images.githubusercontent.com/43708486/219961196-755f49d2-3ba8-430d-8896-9f5950d9875d.png)

## Step 5.

Now click the "API credentials" rider and then "Install app".

![image](https://user-images.githubusercontent.com/43708486/219961381-a32c4724-c2a1-49f7-b052-986d2263ae70.png)

## Step 6.

Copy the *API access token*, *API key* and *API secret key*, keep them at a secure place and send it in a secure/encrypted way to the zerp operator. 

![image](https://user-images.githubusercontent.com/43708486/219961465-6d805769-0e22-45cc-a4d4-880f59d08fc2.png)

## Step 7.

Now go to "Locations" and choose the Location (i.e. Storage) that shall be linked to the Zalando inventory. Ideally you anyway only have one location/storage.
The choosen location's inventory is then synced to Zalando's inventory.

![image](https://user-images.githubusercontent.com/43708486/219961685-4cfd08a5-a75d-46af-ba40-f4005d1b511c.png)

## Step 8.

Copy the location ID that is visible at the end of the URL once clicked on the location.
Send this ID to the zerp operator.

```
https://admin.shopify.com/store/zalandointegrationtestshop/settings/locations/**<HERE IS THE LOCATION ID>**
```

## Wrap up

Zerp is now all set to sync the Zalando and Shopify stores and create Shopify orders (takes some days).  
Once the products are successfully onboarded and unblocked by Zalando, they are live on the marketplace and the sync directly works.  
All further modus operandi are then discussed on an individual level.
















