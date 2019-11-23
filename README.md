
# /react-native-sms-retriever-api

## Getting started

`$ npm install react-native-sms-retriever-api --save`

### Mostly automatic installation

`$ react-native link react-native-sms-retriever-api`

### Manual installation


<!-- #### iOS  Not Required

1. In XCode, in the project navigator, right click `Libraries` ➜ `Add Files to [your project's name]`
2. Go to `node_modules` ➜ `react-native-sms-retriever` and add `RNSmsRetriever.xcodeproj`
3. In XCode, in the project navigator, select your project. Add `libRNSmsRetriever.a` to your project's `Build Phases` ➜ `Link Binary With Libraries`
4. Run your project (`Cmd+R`)< -->

#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`
  - Add `import com.smsretriever.RNSmsRetrieverPackage;` to the imports at the top of the file
  - Add `new RNSmsRetrieverPackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-sms-retriever-api'
  	project(':react-native-sms-retriever-api').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-sms-retriever-api/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-sms-retriever-api')
  	```


## Methods

---
### `getOtp():Promise<boolean>`

Start listening for OTP/SMS. Return true if listener starts else throws error.

---
### `getHash():Promise<string[]>`

Gets the hash code for the application which should be added at the end of message.
This is just a one time process.

---
### `addListener(handler:(message:string)=>any):Promise<boolean>`

Adds a javascript listener to the handler passed which is called when message is received.

---
### `removeListener():void`

Removes the listener.

## Usage
```javascript
import RNSmsRetriever from 'react-native-sms-retriever-api';

// TODO: What to do with the module?





```
  
