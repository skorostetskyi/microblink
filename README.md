
## 1. Requirements

Xcode 10.2
Swift 4.2

## 2. Folder Structure

Inside `PassbaseiOSDemo` are all the files of the demo application. 
Please first install the SDK locally before starting to develop.

## 3. Installation

To install the SDK please first install Cocoapods on your machine. You can find a guide for that [here](https://stackoverflow.com/questions/20755044/how-to-install-cocoapods). Afterwards, open the Podfile of this project and ensure that the following lines are in / adjust the second one here.

```ruby
# Add to the very top of Podfile
source 'https://github.com/facetec/cocoapods-specs.git'

# Add after target xxx do
pod 'Passbase', :path => '/Users/mathiasklenk/passbase-dev/ios-sdk'
```
Check here for `/Users/mathiasklenk/passbase-dev/ios-sdk`. This should be the path where your local SDK project lies on your machine. In the above code example it is where I cloned the Passbase SDK project to, so user `mathiasklenk` and then in the folder `passbase-dev` and `ios-sdk`. 

After that, open your terminal, cd into this demo application `PassbaseiOSDemo` and run the following command.

`pod install`

This will create a new file called `PassbaseiOSDemo.xcworkspace` inside your project directory. Close the existing `PassbaseiOSDemo.xcodeproj` if you opened it previously and start using the `PassbaseiOSDemo.xcworkspace` file. This is your new workspace file with the installed dependencies.


## 4. Developing

Now that you successfully installed the SDK and integrated it locally into your demo project, you can click on the folder structure on Pods. This is where the  dependencies are in. You will find a folder called `Development Pods` here. In here are all the local files of the SDK that you can change. 

Inside `Passbase` are all the classes of the SDK. Inside `Resources/Classes` are thee storyboards and xibs, inside `Resources/Resources` are the images, gifs, fonts etc.

For a detailed developing description, also check out the [SDK project](https://gitlab.com/passbase/passbase-ios-sdk) itself. 

**IMPORTANT:** You can locally change the classes in this project. If you want to build and run the demo application, please always ensure to clean build the project (CMD + Shift + K) and then run it again (CMD + R). This is because Xcode caches the Pods and dependencies. So in order to see the changes in the App, we have to reinstall the Demo App incl. SDKs completely fresh. 


## 5. Deployment


There is no real deployment since this is a demo project and you can technically use any other project where you try to integrate the SDK.

## Author

Mathias J. Klenk, mathias@passbase.com

## License

Passbase is available under the MIT license. See the LICENSE file for more info.
