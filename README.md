# cordova-plugin-appinfo

Cordova plugin based on Dan Michaelo's appInfo plugin (https://github.com/danmichaelo/cordova-plugin-appinfo) that provides access to the following app info:

* `identifier`: Bundle Identifier on iOS, PackageName on Android. Example: `'com.ecolab.PrepNPrintFlex'`.
* `version`: CFBundleVersion on iOS, versionName on Android, Version from WMAppManifest.xml on WP8. Example: `'1.0.2'`.
* `build`: Build on iOS (Example: `'1.0.2.1'`), versionCode on Android (Example: `'18'`), empty string on WP8 (not supported).
* `buildDate`: date of classes.dex on Android in MMddHHmm format (Example: `'02051307'`).

### Installation

Download to your hard drive and add it to your solution.

### Supported Platforms

- Android
- iPhone
- WP8 (except build number)

### Example

```js
navigator.appInfo.getAppInfo(function(appInfo) {
  console.log('identifier: %s', appInfo.identifier);
  console.log('version: %s', appInfo.version);
  console.log('build: %s', appInfo.build);
  console.log('buildDate: %s', appInfo.buildDate);
}, function(err) {
	alert(err);
});
```

### Contributing

Pull requests are welcome.

* @torjo2k added the build Date
* @thomas-mullaly added the WP8 implementation
* @yezhiming added functionality to get identifier and build.

