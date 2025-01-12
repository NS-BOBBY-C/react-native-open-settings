# @bobbycolley/react-native-open-settings

Forked and up-to-date package for [react-native-open-settings](https://github.com/lunarmayor/react-native-open-settings)

[![npm version](https://badge.fury.io/js/%40bobbycolley%2Freact-native-open-settings.svg)](https://badge.fury.io/js/%40bobbycolley%2Freact-native-open-settings)

Open your apps settings in the Settings app

## Install

### Yarn

```bash
yarn add @bobbycolley/react-native-open-settings
```

### NPM

```bash
npm install @bobbycolley/react-native-open-settings
```

## Setup

### Autolinking

### iOS

```bash
cd ios
pod install
```

Thats it! You don't need to do anything else.

### Manual Setup

#### iOS

Add `React Native Open Settings` to project libraries.

#### Android

- Edit `build.gradle` to look like this:

```java
apply plugin: 'com.android.application'

android {
  ...
}

dependencies {
  ...
+ compile project(':react-native-open-settings')
}
```

- In `settings.gradle`, insert the following code:

```java
include ':react-native-open-settings'
project(':react-native-open-settings').projectDir = new File(rootProject.projectDir, '../node_modules/react-native-open-settings/android')
```

- Edit your `MainApplication.java` to look like this:

```java
package com.myapp;

....
import com.opensettings.OpenSettingsPackage

public class MainApplication extends Application implements ReactApplication {

    @Override
    protected List<ReactPackage> getPackages() {
        return Arrays.<ReactPackage>asList(
                new MainReactPackage(),
                new OpenSettingsPackage()
        );
    }
    ...
}
```

## Usage

Require the `@bobbycolley/react-native-open-settings` module.

```javascript
import OpenSettings from "@bobbycolley/react-native-open-settings";
```

And then, where you want to open the settings, just do

```javascript
OpenSettings.openSettings();
```

Have fun!

## TODO

- [x] Update README
- [x] Add MIT License
- [x] Update with PR's from react-native-open-settings
- [ ] New features
- [ ] Add tests
