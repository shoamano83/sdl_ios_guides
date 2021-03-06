## Installation
In order to build your app on a SmartDeviceLink (SDL) Core, the SDL software development kit (SDK) must be installed in your app. The following steps will guide you through adding the SDL SDK to your workspace and configuring the environment.

### Install SDL SDK
We have provided three different ways to install the SDL SDK in your project: CocoaPods, Carthage, or manually.

#### CocoaPods Installation
1. Xcode should be closed for the following steps.
2. Open the terminal app on your Mac.
3. Make sure you have the latest version of [CocoaPods](https://cocoapods.org) installed. For more information on installing CocoaPods on your system please consult: [https://cocoapods.org](https://cocoapods.org).
```
sudo gem install cocoapods
```

4. Navigate to the root directory of your app. Make sure your current folder contains the **.xcodeproj** file
5. Create a new **Podfile**.
```
pod init
```

6. In the **Podfile**, add the following text. This tells CocoaPods to install SDL SDK for iOS.
```
target ‘<#Your Project Name#>’ do
    pod ‘SmartDeviceLink’, ‘~> <#SDL Version#>’
end
```
!!! NOTE
SDL Versions are available on [Github](https://github.com/smartdevicelink/sdl_ios/releases). We suggest always using the latest release.
!!!

7. Install SDL SDK for iOS:  
```
pod install
```
8. There will be a newly created **.xcworkspace** file in the directory in addition to the **.xcodeproj** file. Always use the **.xcworkspace** file from now on.
9. Open the **.xcworkspace** file. To open from the  terminal, type:  
```
open <#Your Project Name#>.xcworkspace
```

#### Carthage Installation
SDL iOS supports Carthage! Install using Carthage by following [this guide](https://github.com/Carthage/Carthage#adding-frameworks-to-an-application).

#### Manual Installation
Tagged to our releases is a dynamic framework file that can be drag-and-dropped into the application. **Please Note: You cannot submit your app to the app store with the framework as is. You MUST strip the simulator part of the framework first. Use a script such as Carthage's to accomplish this.**
