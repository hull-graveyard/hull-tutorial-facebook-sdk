---
title: Integration with the Facebook SDK
subtitle: This tutorial explains how to integrate more deeply Hull and the Facebook SDK to subscribe to events and track like button activity for instance.
---

# tl;dr;
Most of the times, the Facebook proxy we provide will be good enough for you, but sometimes you want a deeper integration, for instance to track Like buttons with XFBML markup and listen to their events. Here's how you can do that.

## What Hull does automatically

By default, Hull handles the facebook SDK so you don't have to set it up in your page, and lets you perform `FB.api` calls through it's proxy:

```js
Hull.api({
  provider:'facebook'
  path: '/me/friends'
}).then(function(res){
  console.log('Facebook Response', res)
});
```

In addition, we emit standardized events and do the tracking for all login and logout events.

## Listening to Facebook events and funneling them through Hull

**Here's how you can access all of the Facebook's SDK features**

This will let you listen to Facebook's events and do tracking calls and integrate with Hull's event system. Future implementations will handle this with less code.

##### To make this work:

* Use the code below and replace your App ID, Org URL by those of your Hull App, 
* Replace `FACEBOOK_APP_ID` by the one from your facebook app.
* In your Facebook App's dashboard (on http://developers.facebook.com), go to "Settings > App Domains" and add your user-facing domain in addition to the Hull organization URL.
* Insert your end-user domain in one of the following fields: "Canvas URL" or "Page Tab" (You probably already have done this already)

Look at the code in Indexy
