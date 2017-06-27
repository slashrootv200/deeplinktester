## Deeplink Tester
1. Use the rocket button in the action bar to attempt to open the entered deeplink
1. Use the download (cloud) button in action bar to download a deeplink json file. see deeplink-json section below for more detials
1. Use the paste (pad) button in action bar to paste a deeplink copied in clipboard instead of manually pasting deeplink in relevant `AutoCompleteTextView`.


![App Screenshot](https://github.com/slashrootv200/deeplinktester/blob/master/deeplinks.png?raw=true "App Screenshot")

### deeplink-json

Below is a sample deeplink json for `vimeo` [android app](https://play.google.com/store/apps/details?id=com.vimeo.android.videoapp)

```json
{
  "schemes": [
    "vimeo"
  ],
  "hosts": [
    "app.vimeo.com"
  ],
  "paths": [
    "videos/12345",
    "users/123",
    "categories",
    "explore",
    "feed",
    "me",
    "notifications",
    "settings/notifications",
    "offline",
    "playlists",
    "purchases",
    "upload"
  ],
  "get_params_keys": [

  ]
}
```
This json is hosted @ [https://api.myjson.com/bins/aclrv](https://api.myjson.com/bins/aclrv). 
1. Copy this URL
1. Tap on the cloud (download icon)
1. A dialog having EditText opens. Paste this URL in the EditText
1. Click on fetch json
1. Now the Deeplink Tester app is configured to autocomplete the relevant deeplink paths / hosts / schemes and even query params if provided in the json.

That's it now deeplink tested is configured to test vimeo android app. You can create jsons for the app you are testing as you would know all the possible values of schemes, hosts, paths and query params for your app. Host the json @ [http://myjson.com/](http://myjson.com/) and then use it to configure the Deeplink tester for your app.

### Tip

Use the deeplink tester with [Push Bullet](https://play.google.com/store/apps/details?id=com.pushbullet.android) android app. This app makes it easy to send deeplinks from your workstation (chrome browser) to you android device, which can then be easily copied and paste in the `Deeplink Tester` app using the `paste icon`
