# react-native-cli-commands
List of react native commands

"scripts": {
"clean": "watchman watch-del-all && rm -rf node_modules && yarn install && yarn cache clean && npx react-native link",
"androidClean": "cd android && ./gradlew clean && cd ../",
"resetCacheStart": "react-native start --reset-cache",
"devMenu": "adb shell input keyevent 82",
"iOSClean": "cd ios && rm -rf Pods/ && rm Podfile.lock && pod install && cd ..",
"cleanAll": "npm run clean && npm run androidClean && npm run iOSClean",
"prepAPK": "npx jetify && react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle && cd ./android && ./gradlew app:assembleRelease",
"PrepIPA": "npx react-native bundle --entry-file index.js --platform ios --dev false --bundle-output ios/main.jsbundle --assets-dest ios",
"android": "react-native run-android",
"ios": "react-native run-ios",
"start": "react-native start"
},
