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