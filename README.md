# hello-ionic2

Documents of ionic2: http://ionicframework.com/docs/v2/

Documents of angular2: https://angular.io/

```python
$ npm install -g ionic@beta

$ ionic start hello-ionic2 tutorial --v2
$ cd MyIonic2Project/
$ ionic serve
```

Building to a Device:
```python
$ sudo npm install -g cordova
```
Building for iOS
```python
$ ionic platform add ios
$ ionic emulate ios
```
Building for Android
```python
$ ionic platform add android
$ ionic run android
```
---

# First build when checkout finished
```python
$ npm install
$ ionic serve
```

# Integrate Cordova Crosswalk plugin
```python
$ ionic platform add android
$ ionic plugin add cordova-plugin-crosswalk-webview
$ ionic build android

Once build successful let you check apk file in:
hello-ionic2/platforms/android/build/outputs/apk
android-armv7-debug-unaligned.apk
android-armv7-debug.apk
android-x86-debug-unaligned.apk
android-x86-debug.apk
```
---

# Icon and Splash Screen Image Generation from the CLI
http://ionicframework.com/docs/cli/icon-splashscreen.html

Create 2 file with name icon.png (192x192 px) and splash.png (2208x2208 px) in hello-ionic2/resources folder.
Run this command auto generator icon and splash to cache
```python
$ ionic resources
```
Run this the second time to transfer to folder
```python
$ ionic resources
```

You can use separate command: 
```python
$ ionic resources --splash
$ ionic resources --icon
```

Once generate successful, let you check in resources folder, some files was generated. 

Run build command to build resources to platform
```python
$ ionic build android
```

Configuration show splash screen in config.xml
```xml
<preference name="AutoHideSplashScreen" value="false"/>
<preference name="SplashScreen" value="screen"/>
<preference name="SplashScreenDelay" value="10000" />
```
So, now config.xml file look like: 
```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<widget id="com.nhancv.ionicv2" version="0.0.1" xmlns="http://www.w3.org/ns/widgets" xmlns:cdv="http://cordova.apache.org/ns/1.0">
  <name>IonicV2 Test</name>
  <description>Project use ionic v2 framework and cordova for building.</description>
  <author email="nhancv1992@gmail.com" href="http://nhancv1992.github.io/">Cao Van Nhan</author>
  <content src="index.html"/>
  <access origin="*"/>
  <allow-intent href="http://*/*"/>
  <allow-intent href="https://*/*"/>
  <allow-intent href="tel:*"/>
  <allow-intent href="sms:*"/>
  <allow-intent href="mailto:*"/>
  <allow-intent href="geo:*"/>
  <platform name="android">
    <allow-intent href="market:*"/>
    <icon src="resources/android/icon/drawable-ldpi-icon.png" density="ldpi"/>
    <icon src="resources/android/icon/drawable-mdpi-icon.png" density="mdpi"/>
    <icon src="resources/android/icon/drawable-hdpi-icon.png" density="hdpi"/>
    <icon src="resources/android/icon/drawable-xhdpi-icon.png" density="xhdpi"/>
    <icon src="resources/android/icon/drawable-xxhdpi-icon.png" density="xxhdpi"/>
    <icon src="resources/android/icon/drawable-xxxhdpi-icon.png" density="xxxhdpi"/>
    <splash src="resources/android/splash/drawable-land-ldpi-screen.png" density="land-ldpi"/>
    <splash src="resources/android/splash/drawable-land-mdpi-screen.png" density="land-mdpi"/>
    <splash src="resources/android/splash/drawable-land-hdpi-screen.png" density="land-hdpi"/>
    <splash src="resources/android/splash/drawable-land-xhdpi-screen.png" density="land-xhdpi"/>
    <splash src="resources/android/splash/drawable-land-xxhdpi-screen.png" density="land-xxhdpi"/>
    <splash src="resources/android/splash/drawable-land-xxxhdpi-screen.png" density="land-xxxhdpi"/>
    <splash src="resources/android/splash/drawable-port-ldpi-screen.png" density="port-ldpi"/>
    <splash src="resources/android/splash/drawable-port-mdpi-screen.png" density="port-mdpi"/>
    <splash src="resources/android/splash/drawable-port-hdpi-screen.png" density="port-hdpi"/>
    <splash src="resources/android/splash/drawable-port-xhdpi-screen.png" density="port-xhdpi"/>
    <splash src="resources/android/splash/drawable-port-xxhdpi-screen.png" density="port-xxhdpi"/>
    <splash src="resources/android/splash/drawable-port-xxxhdpi-screen.png" density="port-xxxhdpi"/>
  </platform>
  <platform name="ios">
    <allow-intent href="itms:*"/>
    <allow-intent href="itms-apps:*"/>
    <icon src="resources/ios/icon/icon.png" width="57" height="57"/>
    <icon src="resources/ios/icon/icon@2x.png" width="114" height="114"/>
    <icon src="resources/ios/icon/icon-40.png" width="40" height="40"/>
    <icon src="resources/ios/icon/icon-40@2x.png" width="80" height="80"/>
    <icon src="resources/ios/icon/icon-50.png" width="50" height="50"/>
    <icon src="resources/ios/icon/icon-50@2x.png" width="100" height="100"/>
    <icon src="resources/ios/icon/icon-60.png" width="60" height="60"/>
    <icon src="resources/ios/icon/icon-60@2x.png" width="120" height="120"/>
    <icon src="resources/ios/icon/icon-60@3x.png" width="180" height="180"/>
    <icon src="resources/ios/icon/icon-72.png" width="72" height="72"/>
    <icon src="resources/ios/icon/icon-72@2x.png" width="144" height="144"/>
    <icon src="resources/ios/icon/icon-76.png" width="76" height="76"/>
    <icon src="resources/ios/icon/icon-76@2x.png" width="152" height="152"/>
    <icon src="resources/ios/icon/icon-small.png" width="29" height="29"/>
    <icon src="resources/ios/icon/icon-small@2x.png" width="58" height="58"/>
    <icon src="resources/ios/icon/icon-small@3x.png" width="87" height="87"/>
    <splash src="resources/ios/splash/Default-568h@2x~iphone.png" width="640" height="1136"/>
    <splash src="resources/ios/splash/Default-667h.png" width="750" height="1334"/>
    <splash src="resources/ios/splash/Default-736h.png" width="1242" height="2208"/>
    <splash src="resources/ios/splash/Default-Landscape-736h.png" width="2208" height="1242"/>
    <splash src="resources/ios/splash/Default-Landscape@2x~ipad.png" width="2048" height="1536"/>
    <splash src="resources/ios/splash/Default-Landscape~ipad.png" width="1024" height="768"/>
    <splash src="resources/ios/splash/Default-Portrait@2x~ipad.png" width="1536" height="2048"/>
    <splash src="resources/ios/splash/Default-Portrait~ipad.png" width="768" height="1024"/>
    <splash src="resources/ios/splash/Default@2x~iphone.png" width="640" height="960"/>
    <splash src="resources/ios/splash/Default~iphone.png" width="320" height="480"/>
  </platform>
  <preference name="webviewbounce" value="false"/>
  <preference name="UIWebViewBounce" value="false"/>
  <preference name="DisallowOverscroll" value="true"/>
  <preference name="android-minSdkVersion" value="16"/>
  <preference name="BackupWebStorage" value="none"/>
  <preference name="xwalkVersion" value="17+"/>
  <preference name="xwalkCommandLine" value="--disable-pull-to-refresh-effect"/>
  <preference name="xwalkMode" value="embedded"/>
  <preference name="xwalkMultipleApk" value="true"/>
  <preference name="SplashScreen" value="screen"/>
  <preference name="SplashScreenDelay" value="3000"/>
  <feature name="StatusBar">
    <param name="ios-package" onload="true" value="CDVStatusBar"/>
  </feature>
  <plugin name="cordova-plugin-device" spec="~1.1.1"/>
  <plugin name="cordova-plugin-console" spec="~1.0.2"/>
  <plugin name="cordova-plugin-whitelist" spec="~1.2.1"/>
  <plugin name="cordova-plugin-splashscreen" spec="~3.1.0"/>
  <plugin name="cordova-plugin-statusbar" spec="~2.1.2"/>
  <plugin name="ionic-plugin-keyboard" spec="~2.0.1"/>

  <preference name="AutoHideSplashScreen" value="false"/>
  <preference name="SplashScreen" value="screen"/>
  <preference name="SplashScreenDelay" value="10000" />
  
  <icon src="resources/android/icon/drawable-xhdpi-icon.png"/>
</widget>
```
---
# Local storage
Ref: https://github.com/rrgarciach/angular2-local-storage

**Usage**
```js
import {LocalStorage} from '../../utils/local-storage';

......


var test = new LocalStorage();
        test.set("test", "test");
        test.clearAll();
```
Support: get, set, getObject, setObject, remove by key, clearAll


# IndexedDB
Ref: https://github.com/gilf/angular2-indexeddb

Usage
-----
Include **angular2-indexeddb.js** in your application.

```html
<script src="components/angular2-indexeddb/angular2-indexeddb.js"></script>
```

Import the the `AngularIndexedDB` class as a dependency:

```js
import {AngularIndexedDB} from './angular2-indexeddb';
```

### AngularIndexedDB service
First instantiate the service as follows:
```js
let db = new AngularIndexedDB('myDb', 1);
```
The first argument is the name of your database and the second is the database version.
If you forget the version you the service will default to version 1.

Use the APIs that the AngularIndexedDB service exposes to use indexeddb.
In the API the following functions:
* createStore(version, createCallback): initializes objectStore/s.
The first parameter is the version to upgrade the database and the second one is a callback the will handle the creation of objectStores for that version.
**createStore** returns a promise that is resolved when the store updated or rejected if an error occurred.

Usage example:

```js
db.createStore(1, (evt) => {
    let objectStore = evt.currentTarget.result.createObjectStore(
        'people', { keyPath: "id", autoIncrement: true });

    objectStore.createIndex("name", "name", { unique: false });
    objectStore.createIndex("email", "email", { unique: true });
});
```
* getByKey(storeName, key): returns the object that is stored in the objectStore by its key.
The first parameter is the store name to query and the second one is the object's key.
**getByKey** returns a promise that is resolved when we have the object or rejected if an error occurred.

Usage example:

```js
db.getByKey('people', 1).then((person) => {
    console.log(person);
}, (error) => {
    console.log(error);
});
```

* getAll(storeName): returns an array of all the items in the given objectStore.
The first parameter is the store name to query.
**getAll** returns a promise that is resolved when we have the array of items or rejected if an error occurred.

Usage example:

```js
db.getAll('people').then((people) => {
    console.log(people);
}, (error) => {
    console.log(people);
});
```

* getByIndex(storeName, indexName, key): returns an stored item using an objectStore's index.
The first parameter is the store name to query, the second parameter is the index and third parameter is the item to query.
**getByIndex** returns a promise that is resolved when the item successfully returned or rejected if an error occurred.

Usage example:

```js
db.getByIndex('people', 'name', 'Dave').then((person) => {
    console.log(person);
}, (error) => {
    console.log(error);
});
```

* add(storeName, value, key): Adds to the given objectStore the key and value pair.
The first parameter is the store name to modify, the second parameter is the value and the third parameter is the key (if not auto-generated).
**add** returns a promise that is resolved when the value was added or rejected if an error occurred.

Usage example (add without a key):

```js
db.add('people', { name: 'name', email: 'email' }).then(() => {
    // Do something after the value was added
}, (error) => {
    console.log(error);
});
```
In the previous example I'm using undefined as the key because the key is configured in the objectStore as auto-generated.

* upsert(storeName, value, key?): Updates the given value in the objectStore. If key is main key or index, it can't be updated.
The first parameter is the store name to modify, the second parameter is the value to update and the third parameter is the key (if there is no key don't provide it).
**upsert** returns a promise that is resolved when the value was updated or rejected if an error occurred.

Usage example (update without a key):

```js
db.upsert('people', { id: 3, name: 'name', email: 'email' }).then(() => {
    // Do something after update
}, (error) => {
    console.log(error);
});
```

* remove(storeName, key): Removes the object that correspond with the key from the objectStore.
The first parameter is the store name to modify and the second parameter is the key to remove.
**remove** returns a promise that is resolved when the value was removed or rejected if an error occurred.

Usage example:

```js
db.remove('people', 3).then(() => {
    // Do something after remove
}, (error) => {
    console.log(error);
});
```

* openCursor(storeName, cursorCallback): opens an objectStore cursor to enable iterating on the objectStore.
The first parameter is the store name and the second parameter callback function to run when the cursor succeeds to be opened.
**openCursor** returns a promise that is resolved when the cursor finishes running or rejected if an error occurred.

Usage example:

```js
db.openCursor('people', (evt) => {
    var cursor = evt.target.result;
    if(cursor) {
        console.log(cursor.value);
        cursor.continue();
    } else {
        console.log('Entries all displayed.');
    }
});

```

* clear(storeName): clears all the data in an objectStore.
The first parameter is the store name to clear.
**clear** returns a promise that is resolved when the objectStore was cleared or rejected if an error occurred.

Usage example:

```js
db.clear('people').then(() => {
    // Do something after clear
}, (error) => {
    console.log(error);
});
```

