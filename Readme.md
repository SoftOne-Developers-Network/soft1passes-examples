# soft1passes-examples

This repo contains simple examples (the body requests) of each Pass Category (Generic, Coupon, StoreCard and EventTicket).

## Getting Started

### Execute the examples

* Login to Soft1Passes
* Execute a SetTemplate.json in [Soft1Passes SetTemplate Endpoint](https://s1passes.softone.gr/docs/#post-/s1epass/SetTemplate).
* Execute a CreatePass.json in [Soft1Passes CreatePass Endpoint](https://s1passes.softone.gr/docs/#post-/s1epass/CreatePass).
* Take the result link from the abouve CreatePass Endpoint and Open it in your Android/iOS Device.
* You should see the pass in your screen

### Update a Pass

* In order to update a pass, just send the same (full body json) SetTemplate or CreatePass with the updated values.
* User can get the latest update version of the pass from his Android/iOS Device. He can do it by "Pull Refresh" action inside the back side of the Pass.

## Push Notification
You can also inform the user for a change in his Pass by a Push Notification.
You need first to make a change to the Pass. Only if you change a value in a Pass the User can see a Push Notification in his Lock Screen.
Push Notification Endpoint: https://s1passes.softone.gr/docs/#post-/s1epass/NotifyDevices

## Important

**To get a new account for Soft1Passes please contact with Softone Technologies S.A.**


⚠️ Everywhere you see `<token>` in body requests you need to change it with your clientId. 
Soft1Passes generates a clientId when you successfully Login through the API.
Login EndPoint: https://s1passes.softone.gr/docs/#post-/s1epass/Login



⚠️ Change the `<template_pk>` with `template` value from the result of the `/SetTemplate`.

In a `/SetTemplate` response the `<template_pk>` is here:

```json
{
    "success": true,
    "message": "UPDATED",
    "template": {
        "template": "<template_pk>"
    }
}
``` 


## Help
You should take a look at Soft1Passes's documentation in order to learn how to communicate with our Service.
Soft1Passes Documentation: https://s1passes.softone.gr/docs/
