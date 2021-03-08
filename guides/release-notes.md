# Release Notes

We're always adding and updating the Velo APIs, and we want you to have one place to find all of our latest changes and cool additions.

We love hearing your feedback! 
Lots of our bugs come from users like you and you can help us improve the docs by reporting them to us. You can report bugs and other feedback through these links found at the bottom of our docs.

![](../media/feedback.png)

We also keep a list of **doc bugs** that are in our backlog, with information that can be helpful to our users even before they are fixed. You can see them [here](https://view.monday.com/97005963-d254f39325f60e6d86ffb64c39192f84).

## New! 🗓️ March 7, 2021

### New API Reference Feature: Show Members open by default

The table that lists the properties in a returned object used to be closed by default and would require you to click **Show Members** to view it. The expandable is now open by default. You can see an example in the **Returns** table for [`createProduct`](https://www.wix.com/velo/reference/wix-stores-backend/createproduct).

### New Release Notes information

We will now label the latest updates in the Release Notes with **New!** in the heading to make it easier to find the latest changes. 

## New! 🗓️ March 4, 2021

### Updated: Remove mention of currentItem from the context of some data hooks

`wix-data`

The `context.currentItem` parameter is only relevant for `beforeUpdate()` and `beforeRemove()` hooks. The property was removed from the documentation for all other hooks.

## New! 🗓️ March 2, 2021

### New API: Bookings Events

`wix-bookings-backend`

[Backend events](https://www.wix.com/velo/reference/wix-bookings-backend/events) have been added to Wix Bookings.
The events  are fired for the following actions:

* A new booking request is created.
* A booking request is confirmed or declined.
* A booking is canceled.
* A booking  schedule is updated.
* Booking attendance information is updated.

### Update: Clarified opacity and hidden for timeline

`wix-animations`

* Updated the target parameter type to `Element` from `mixin`.  
* Clarified that only elements that mix in the `hiddenMixin` can be the target.
* Clarified that the unit for opacity is from 0.0 - 1.0.

## New! 🗓️ February 22, 2021

### New API: Price per unit data fields added to product object

`wix-stores-backend`

Price Per Unit data fields were added to APIs returning product objects and product variant objects. These APIs mirror the Dashboard feature that allows you to display a product's base and total quantity/weight/area. Complies with requirements in the German market.

## New! 🗓️ February 7, 2021

### New API: Pricing Plans: Plan management

`wix-pricing-plans-backend`

With the new [pricing-plans-backend](https://www.wix.com/velo/reference/wix-pricing-plans-backend) APIs, you can manage your APIs in ways that before, you could only do from the Dashboard.

Now you can create, update, hide, and archive pricing plans. You can set and clear which pricing plan is the primary plan and rearrange the order in which plans are displayed on the site. And we now supply different ways for you to get information about existing plans, such as getting a single plan, getting statistics for a plan, listing public/all plans, and performing queries. 

## 🗓️ February 3, 2021

### New API Reference Feature: Release Notes change indicator

A red dot now appears next to the **Release Notes** section in the left tree when it is updated. More enhancements on the way.

### Updated: getSecret does not require Members Area

`wix-secret-backend`

We removed a note that said you need the Members Area on your site to work with the [`getSecret()`](https://www.wix.com/velo/reference/wix-secrets-backend/getsecret) API.

### Updated: Slot Id parameter fixed

`wix-bookings`

We changed `slot_id` to `slotId` in [`getCheckoutOptions()`](https://www.wix.com/velo/reference/wix-bookings/getcheckoutoptions).

### Updated: getCurrentMemberOrders returns a promise

`wix-paid-plans`

[`getCurrentMemberOrders()`](https://www.wix.com/velo/reference/wix-paid-plans/getcurrentmemberorders) returns a promise that resolves to an array. We previously stated that the function returns an array.

### Updated: cancelOrder throws an error

`wix-paid-plans`

We clarified that [`cancelOrder`](https://www.wix.com/velo/reference/wix-paid-plans/cancelorder) throws an error when **[Allow Plan Cancellation](https://support.wix.com/en/article/pricing-plans-allowing-clients-to-cancel-plans)** is set to False in the Dashboard.

### Updated: Recommend using getCurrentGeolocation with setTimeout

`wix-window`

In cases where the site visitor's browser is set to not detect locale, the promise does not resolve or reject. We added a note recommending using [`getCurrentGeoLocation()`](https://www.wix.com/velo/reference/wix-window/getcurrentgeolocation) with `setTimeout` to handle the unresolved Promise.

### Updated: Hooks run when data is imported

`wix-data`

We added a note that the [`beforeInsert`](https://www.wix.com/velo/reference/wix-data/hooks/beforeinsert) and [`afterInsert`](https://www.wix.com/velo/reference/wix-data/hooks/afterinsert) hooks run when data is imported to either Live or Sandbox collections.

### Updated: queryReferenced() only works with multiple-item reference fields

`wix-data`

We added a note that you can only use the [`queryReferenced()`](https://www.wix.com/velo/reference/wix-data/queryreferenced) function with multiple-item reference fields and not with single-item (regular) reference fields.

### Updated: Use the checked property with the Switch element

`Wix Editor Elements ($w)`

The `value` property does not work with the [`Switch`](https://www.wix.com/velo/reference/w/switch) element. We added a note to use the `checked` property instead. We also added an example for using the `checked` property to set the `Switch` state.

### Updated: RichTextBox does not support KeyboardEvent and onInput

`Wix Editor Elements ($w)`

`KeyboardEvent` doesn’t fire and `onInput` is not supported for [`RichTextBox`](https://www.wix.com/velo/reference/w/richtextbox) elements. We removed a reference to the `RichTextBox` element from the `KeyboardEvent` documentation and added a note to `onInput` that it is not supported for `RichTextBox` elements.

### Updated: SelectionTags options property changes

`Wix Editor Elements ($w)`

Setting the [`options`](https://www.wix.com/velo/reference/$w/selectiontags/options) property no longer clears the `value` and `selectedIndices` of the selection tags. This allows users to add and reorder choices without clearing the visitor's selection. Only values that no longer match the new options are cleared.

Setting `value` no longer lets you set values that do not match any of the options.

### Updated: formattedPrice and formattedDiscountedPrice are read-only

`wix-stores-backend`

We removed a reference to `formattedPrice` and `formattedDiscountedPrice` fields for [`updateVariantData()`](https://www.wix.com/velo/reference/wix-stores-backend/updatevariantdata) since they are read-only and can't be set.

## 🗓️ January 20, 2021

### Updated: SSL note in wixWindow.openModal() 

`wix-window`

It is not possible to turn SSL off with Velo. We removed a part of the note that was misleading.

## 🗓️ January 19, 2021

### New API: Coupons events

`wix-marketing-backend`

With the new [Coupon backend events](https://www.wix.com/velo/reference/wix-marketing-backend/events) you can write code that is triggered when a coupon is created, updated, deleted, or applied.

### New API: Added appID to Coupons API

`wix-marketing-backend`

Added the `appID` property to the CouponEvent object. The ID of the app that created the coupon. Empty if created by the site owner.

## 🗓️ January 14, 2021

### Updated: updateCustomerInfo deletes any non-updated properties

`wix-bookings-backend`

Updated an example and added a note that [`updateCustomerInfo`](https://www.wix.com/velo/reference/wix-bookings-backend/bookings/updatecustomerinfo) updates the entire object and that any properties not included in the object passed will be deleted.

### New API: Cancel & Refund events

`wix-stores-backend`

With the new [`onOrderRefunded()`](https://www.wix.com/velo/reference/wix-stores-backend/events/onorderrefunded) & [`onOrderCanceled()`](https://www.wix.com/velo/reference/wix-stores-backend/events/onorderrefunded) backend events you can now write code that is triggered when an order is refunded and/or canceled.

## 🗓️ January 12, 2021

### New API: Bookings backend

`wix-bookings-backend`

Backend APIs are now available to manage Bookings. The [`wix-bookings-backend`](https://www.wix.com/velo/reference/wix-bookings-backend) API provides bookings functionality allowing you to:

- List and query booking information.
- Confirm pending booking requests.
- Decline pending booking requests.
- Cancel a booking.
- Set attendance for booked sessions.
- Mark a booking as paid.
- Update the customer's booking information.

## 🗓️ December 31, 2020

### New API: Increment inventory

`wix-stores-backend`

With the new Wix Stores [`incrementInventory()`](https://www.wix.com/velo/reference/wix-stores-backend/incrementinventory) API you can increment a product variant's stock in the store's inventory. Pass a variantId and either a productID or an inventoryId, as well as the integer to increment by.

## 🗓️ December 30, 2020

### Updated: Added multiple locations to ServiceAvailability object

`wix-bookings`

The `ServiceAvailability` object returned by [`getServiceAvailability`](https://www.wix.com/velo/reference/wix-bookings/getserviceavailability) now includes a location property. If the service is offered in multiple locations, a slot is returned for each location.

## 🗓️ December 27, 2020

### Updated: Upload button now indicates if a file fails to upload

`Wix Editor Elements ($w)`

The `valid` property of [`UploadButton`](https://www.wix.com/velo/reference/$w/uploadbutton) is set to `false` when a file fails to upload. Previously this was only set if `required == TRUE`.

### Updated: openLightbox requires onReady

`wix-window`

Even though [`openLightbox`](https://www.wix.com/velo/reference/wix-window/openlightbox) is not part of `$w` it can only be called after the `onReady` event has fired.

### Updated: Wix Data is eventually consistent

`wix-data`

The wix-data API is [eventually consistent](https://www.wix.com/velo/reference/wix-data/introduction#wix-data_introduction_wix-data-and-eventual-consistency), meaning that sometimes updates to your database collection are not immediate. There may be a short delay until the system is up-to-date with your recent changes. During the delay, the data you get back may not reflect those changes.

### API Updated: Added seoData field to the Product object

We added the `seoData` field to the Product object. This mirrors the SEO data added in the dashboard and allows for adding custom SEO tags when using [`createProduct()`](https://www.wix.com/velo/reference/wix-stores-backend/createproduct).

## 🗓️ December 24, 2020

### Updated: Editor elements ($w) progressBar.value is a get or set

`Wix Editor Elements ($w)`

We incorrectly stated that you could only “get” the `value` of the [`ProgressBar`](https://www.wix.com/velo/reference/$w/progressbar/value) element. We clarified that you can both “get” and “set” the `value` property.

### Updated: bulkUpdate clarification

`wix-data`

We were a bit vague about how [`bulkUpdate`](https://www.wix.com/velo/reference/wix-data/bulkupdate) works. We now stress in the explanation that `bulkUpdate` replaces all properties of the existing, matching items. When specifying which properties you want to update, the values of any properties that are not specified are lost.

### New API: privacyStatus property for register function in wix-users and wix-users-backend

`wix-users`

`wix-users-backend`

There is a new privacyStatus parameter for the [`register`](https://www.wix.com/velo/reference/wix-users/register) function. Options are `PUBLIC` and `PRIVATE`.

### Updated: Clarified creation of routers.js file

`wix-router`

The [introduction](https://www.wix.com/velo/reference/wix-router/introduction) implied that the user needs to create the `routers.js` file. Actually, when you set up your router, the file is created for you. We clarified that you do not need to manually create the `routers.js` file.

We also reviewed the existing explanations and made some updates, including: 

- How to work with routers, based on changes made in the Editor. 
- How we explain the URL needed for [WixRouterRequest](https://www.wix.com/velo/reference/wix-router/wixrouterrequest/introduction). 
- Adding and fixing links.
- Fixing a typo in an example.

### New API: wix-users-backend Roles

`wix-users-backend`

We added the [`assignRole()`](https://www.wix.com/velo/reference/wix-users-backend/roles-obj/assignrole) and [`removeRole()`](https://www.wix.com/velo/reference/wix-users-backend/roles-obj/removerole) functions to the new `Roles` API in `wix-users-backend`, allowing you to manage site member access to restricted pages.

### New API: wix-stores addCustomItemsToCart()

`wix-stores`

With the new Wix Stores [addCustomItemsToCart()](https://www.wix.com/velo/reference/wix-stores/addcustomitemstocart) API you can now add custom items that aren't "products" to the cart. For example, an insurance or agent's fee. 


## 🗓️ December 7, 2020

### New API: VideoBox

`Wix Editor Elements ($w)`

Velo's APIs are now available to control how videos play in [`VideoBox`](https://www.wix.com/velo/reference/$w/videobox) elements on your site. Video boxes allow you to showcase your videos in beautifully-designed video containers. Unlike VideoPlayer elements, VideoBox elements do not have controls, text descriptions, titles and cannot be displayed in full screen mode. This gives video boxes a clean look.
You can use the APIs to manage video boxes for: 

- Videos uploaded to your site
- Transparent videos uploaded to your site
- Videos/Transparent videos from the  Wix Media library

### Updated: textInput.maxLength remove max length

`Wix Editor Elements ($w)`

The instructions to remove the [`maximum length`](https://www.wix.com/velo/reference/$w/textinput/maxlength) restriction incorrectly stated to set maxLength to 0. We clarified that you can format the text using the html property.

### Updated: text styles

We listed the supported styles and formats for [`text type elements`](https://www.wix.com/velo/reference/$w/text/introduction) but did not explain how to use them. We clarified that you can format the text using the html property.

### Updated: uploadButton.reset 

`Wix Editor Elements ($w)`

We clarified that the [`reset()`](https://www.wix.com/velo/reference/$w/uploadbutton/reset) function clears the files in the value property.

### Updated: radioButtonGroup options 

`Wix Editor Elements ($w)`

The description incorrectly stated that [`options`](https://www.wix.com/velo/reference/$w/radiobuttongroup/options) is an object. We clarified that options is an array of option objects.

### Updated: getCheckoutOptions slotID

`wix-bookings`

In the [`getCheckoutOptions`](https://www.wix.com/velo/reference/wix-bookings/getcheckoutoptions) parameter table, slot_ID was formatted incorrectly. The correct format is slotID.

### Updated: wixWindow.scrollTo coordinates

`wix-window`

In the [`scrollTo`](https://www.wix.com/velo/reference/wix-window/scrollto) function we didn’t mention how to get the coordinates of a given location. We added how to get the coordinates of a location on the page using the Editor toolbar.

### Updated: wixLocation URL structure

`wix-location`

The layout for describing the different parts of the [`URL`](https://www.wix.com/velo/reference/wix-location/introduction) was a bit confusing. We changed the URL breakdown to match the same layout as the wixHttpFunctionRequest object in the wix-http-functions API for consistency.

## 🗓️ November 1, 2020

### New API: Wix Forum Backend Event APIs

`wix-forum-backend`

With the new [Forum Backend Events](https://www.wix.com/velo/reference/wix-forum-backend) you can react to activity on your forum. You can run custom code when forum categories, posts, and comments are created, updated, deleted, posted, pinned, voted on, liked, reported, and more. For example, you can send a custom email to a poster when their post is liked, display a message when a comment is marked as best, or set up an alert when a post or comment is reported. 

### New API: removeProductFromCart

`wix-stores`

With [`removeProductFromCart()`](https://www.wix.com/velo/reference/wix-stores/removeproductfromcart) you can remove a line item/product from the cart. 

## 🗓️ October 20, 2020

### New API: onWixFormSubmit() event handler in the WixForms API

`wix-crm`

With the new [`onWixFormSubmit()`](https://www.wix.com/velo/reference/wix-crm/$w-wixforms/onwixformsubmit) event handler in the WixForms API, you can perform validations on your forms immediately after visitors submit the form yet before the server starts any processing.  

## 🗓️ October 13, 2020

### Updated: wixLocation.to() does not work in preview

`wix-location`

Added a note that [`wixLocation.to()`](https://www.wix.com/velo/reference/wix-location/to) only works on a published site and not while previewing.

### Updated: htmlComponent can only embed a PDF file with a Premium account

`$w.HtmlComponent`

To embed a PDF in an [HtmlComponent](https://www.wix.com/velo/reference/$w/htmlcomponent/introduction) you must upgrade your site to a Premium Plan.

## 🗓️ October 11, 2020

### New API: Decrement inventory

`wix-stores-backend`

Manually [decrement](https://www.wix.com/velo/reference/wix-stores-backend/decrementinventory) a product variant's stock in inventory. This functionality is helpful for creating an inventory management page on your site.

## 🗓️ September 16, 2020

### Updated: Added Stackdriver information to Site Monitoring introduction

`site-monitoring`

Added [information](https://www.wix.com/velo/reference/spis/site-monitoring/introduction) about connecting Wix site events to Google's Stackdriver external monitoring tool.

## 🗓️ September 15, 2020

### Updated: Changed slider.value from read only to read & write

`$w.slider` 

The [`value`](https://www.wix.com/velo/reference/$w/slider/value) property for the Slider element was described as read only but it should be read and write.

### Updated: Added more information for returned object properties from Validity property

`ValidatableMixin`

Added more content to the table that displays details of the object returned by [`validity`](https://www.wix.com/velo/reference/$w/validatablemixin/validity).

## 🗓️ September 14, 2020

### Updated: Added information that some getProductVariants() parameter fields are optional

`wix-stores`

Added information that some of the parameter fields for [getProductVariants()](https://www.wix.com/velo/reference/wix-stores/getproductvariants) are optional.

### Updated: createProduct() SKU is a string

`stores-backend`

The `sku` property for [createProduct()](https://www.wix.com/velo/reference/wix-stores-backend/createproduct) was described as a number, but it is a string.

## 🗓️ September 10, 2020

### Updated: Added information about getFileURL token expiring

`wix-media-backend`

Added information that the token returned by [`getFileUrl()`](https://www.wix.com/velo/reference/wix-media-backend/mediamanager-obj/getfileurl) expires after 600 minutes. Described the alternative of creating a static URL without a token.

### Updated: The URL table for wixHttpFunctionRequest

`wix-http-functions`

The table that described the URL structure of a [wixHttpFunctionRequest](https://www.wix.com/velo/reference/wix-http-functions/wixhttpfunctionrequest) was difficult to parse. We've updated the content to make it easier to understand. 

## 🗓️ September 7, 2020

### New API: On cart changed event

`wix-stores`

With the new [`onCartChanged()`](https://www.wix.com/velo/reference/wix-stores/oncartchanged) client-side event in wix-stores, you can access information about the site's shopping cart every time an item is added or removed. Useful for creating a promotional lightbox - if product X is added to the cart, offer product Y.

### New API: Consent policy (privacy laws)

`wix-users`

To help your site conform to GDPR and CCPA standards, we now provide Velo APIs for [checking](https://www.wix.com/velo/reference/wix-users/getcurrentconsentpolicy) and [setting](https://www.wix.com/velo/reference/wix-users/setconsentpolicy) visitors' current consent policies. These policies include which cookies the visitor allows and if the visitor allows data transfer to third parties.

## 🗓️ August 30, 2020

### Updated: Added examples to listMemberBadges()

`wix-users-backend`

Added more robust examples to [`listMemberBadges()`](https://www.wix.com/velo/reference/wix-users-backend/badges-obj/listmemberbadges) for how to handle the results.

## 🗓️ August 23, 2020

### New API: Coupon limit per customer

`wix-marketing-backend`

Use the new [limitPerCustomer](https://www.wix.com/velo/reference/wix-marketing-backend/coupons-obj/createcoupon) property that allows for limiting coupon use per customer. Helpful if you'd like to create a coupon to be used only once, or any number of times per customer.

## 🗓️ August 20, 2020

### New API: Custom fulfiller email 

`wix-stores-backend`

Use the new [`sendFulfillmentEmail()`](https://www.wix.com/velo/reference/wix-stores-backend/sendfulfillmentemail) function to send an email containing fulfillment details (products to ship, shipping details, etc.) to a custom fulfiller (a fulfiller not integrated with Wix, like ShipBob or ShipStation). 

### New API: Order paid event 

`wix-stores-backend`

Added a new [event](https://www.wix.com/velo/reference/wix-stores-backend/events/onorderpaid) that fires when an order is marked as paid.

## 🗓️ August 12, 2020

### Updated: New array and object data types

`wix-data`

Added information about new array and object types to the [wix-data Introduction](https://www.wix.com/velo/reference/wix-data/introduction).

## 🗓️ August 11, 2020

### New API: Print packing slip

`wix-stores-backend`

Use the new [`getPackingSlipLink()`](https://www.wix.com/velo/reference/wix-stores-backend/getpackingsliplink) function to generate and print a PDF file of an order's packing slip. Especially useful in the ThankYouPage, after an order is completed.

## 🗓️ August 9, 2020

### Updated: New validations for file upload

`wix-media-backend`

The [Upload](https://www.wix.com/velo/reference/wix-media-backend/mediamanager-obj/upload) button can now perform certain validations right after file selection.

### Updated: Mark createContact() parameters as optional

`wix-crm`

Changed the `contactInfo` parameters for [`createContact()`](https://www.wix.com/velo/reference/wix-crm/createcontact) to be optional.

## 🗓️ August 6, 2020

### New API: Print orders

`wix-stores-backend`

Use the new [`getOrdersLink()`](https://www.wix.com/velo/reference/wix-stores-backend/getorderslink) function to generate a PDF file containing information about one of more of your store's orders.

## 🗓️ August 3, 2020

### Updated: New example for onItemReady()

`$w.repeater`

Added a simple [`onItemReady()`](https://www.wix.com/velo/reference/$w/repeater/onitemready) example where `onItemReady()` is triggered when repeater data is set.

### Updated: New example for WixDataQuery.include()

`wix-data`

Added new example in [`WixData.query.include()`](https://www.wix.com/velo/reference/wix-data/wixdataquery/include) to show how to use a reference field from another collection when populating a table with DataPath.

### Updated: Router examples should use https for imageSite links

`wix-router`

The **A router with static data** example for the [`router()`](https://www.wix.com/velo/reference/wix-router/router) function used http URLs in the example for imageSite. They were updated to use https.


## 🗓️ August 2, 2020

### Updated: Secrets API

`wix-secrets-backend`

With the new [Secrets API functions](https://www.wix.com/velo/reference/wix-secrets-backend) you can manage your site secrets with code. Create, update, and delete secrets in the Secrets Manager programmatically without opening the UI. List all your site secrets to find the one you need.

## 🗓️ July 30, 2020

### New API: Fulfillment

`wix-stores-backend`

Use the [`createFulfillment()`](https://www.wix.com/velo/reference/wix-stores-backend/createfulfillment) function to create, update, and delete order fulfillments (as well as set up events for each).

### New API: Create order

`wix-stores-backend`

Use the [`createOrder()`](https://www.wix.com/velo/reference/wix-stores-backend/createorder) function to have more control over various order properties, allowing for more custom order flows. 

## 🗓️ July 28, 2020

### New API: Form Builder

`wix-crm` `wix-crm-backend`

With the new Wix Forms APIs,  you can access Wix Form app functionality with code. You can customize how site visitors work with the Wix Form, while taking advantage of the Wix Forms app's ease of design, automatic creation of submission collections, payment receipt, automatic setup of email notifications, and more. You can perform actions both on the [client side](https://www.wix.com/velo/reference/wix-crm/$w-wixforms) and in the [backend](https://www.wix.com/velo/reference/wix-crm-backend/events/onformsubmit).

## 🗓️ July 9, 2020

### Updated: Badges

`wix-users-backend`

With the new [Badges APIs](https://www.wix.com/velo/reference/wix-users-backend/badges)  you can manage your member badges with code. Create, update, and delete badges, assign and remove badges from members, and see which members are associated with each badge.

### Updated: Add information about import and export triggering before and after query hooks 

`wix-data`

Added information that [before](https://www.wix.com/velo/reference/wix-data/hooks/beforequery) and [after](https://www.wix.com/velo/reference/wix-data/hooks/afterquery) query hooks are triggered when items are exported from a collection.
