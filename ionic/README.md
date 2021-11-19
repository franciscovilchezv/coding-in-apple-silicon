# Ionic

The LTS Node version is needed for make this work. Do the following steps with out rosetta unless specified in the instructions.

## Create ionic project

Follow the official [website instructions](https://ionicframework.com/getting-started) for creating the project.

### Instal ionic cli natively

`npm install -g @ionic/cli`

### Create the ionic project

`ionic start myApp tabs`

## Install cocoapods natively

`sudo gem install cocoapods`

## Add capacitor with Rosetta

`arch -x86_64 npx cap add ios`

## Open project with xCode and run it

`npx cap open ios`

The OS knows when to use Rosetta if it detects the software has x86 instructions according to [Apple](https://developer.apple.com/documentation/apple_silicon/about_the_rosetta_translation_environment).

## For other tools that need to install

We need `sharp` as mentioned in this [issue](https://github.com/lovell/sharp/issues/2460).

`brew reinstall vips`

After this, we can run

`npm i -g native-run cordova-res`


## Possible errors

```
✔ Updating iOS plugins in 4.32ms
[info] Found 4 Capacitor plugins for ios:
       @capacitor/app@1.0.6
       @capacitor/haptics@1.1.3
       @capacitor/keyboard@1.1.3
       @capacitor/status-bar@1.0.6
✖ Updating iOS native dependencies with pod install - failed!
✖ update ios - failed!
[error] xcode-select: error: tool 'xcodebuild' requires Xcode, but active developer directory
        '/Library/Developer/CommandLineTools' is a command line tools instance
```

Fix it with:

```
sudo xcode-select -s /Applications/Xcode.app/Contents/Developer
sudo xcodebuild -license accept
```
