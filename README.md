
# cordova-outsystems-firebase-analytics
This plugin brings analytics, event tracking and crash reporting from Google Firebase to your Outsystems project!  Android and iOS supported.

## Installation
Install the plugin by adding it to your project's extensibility configuration:

```
{
    "plugin": {
        "url": "https://github.com/OutSystemsExperts/cordova-outsystems-firebase-analytics.git#v1.0.0"
    }
}
```

### Setup
Download your Firebase configuration files, GoogleService-Info.plist for iOS and google-services.json for android, zip them in a file named google-services.zip and place that zip in the resources of your outsystems app with ´google-services´ as the target dir.  Check out this [firebase article](https://support.google.com/firebase/answer/7015592) for details on how to download the files.


###### IMPORTANT NOTES
- This plugin uses a hook (after prepare) that copies the configuration files to the right place.
- Firebase SDK requires the configuration files to be present and valid, otherwise your app will crash on boot or Firebase features won't work.

### Pushwoosh
Your build may fail if you are installing version of cordova-pushwoosh-plugin superior or equal to 7.0.7.  This is caused by the plugins installing different versions of the firebase analytics and the Google Play Services library.  This can be resolved by change the extensibility configuration to use a version of this plugin without-dep.

## API

See the full [API](API.md) available for this plugin.