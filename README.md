# Reproduce example

How to reproduce this error [issue](https://github.com/callstack/react-native-paper/issues/893)

- clone this npm i
- expo start --android
- after its running on emulator/device
- open adb logcat
- refresh and you'll see the error like below
- the crash recovers using expo, but on a production app it displays a white screen when it crashes and then recovers. Resulting in a long startup

![crash image adb](crash.jpg)

# The fix

I made a pull request so you can use my forked branch to test
- checkout fix branch
- remove node_modules
- ```watchman watch-del-all``` just in case
- npm i
- expo start --clear
- after its running on emulator/device
- open adb logcat
- refresh and you'll see the error like below
- should be fixed
