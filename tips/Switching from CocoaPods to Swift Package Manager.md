Title:  Switching from CocoaPods to Swift Package Manager

Tags:   Xcode

Link:   https://swift.org/package-manager/

Text:   Swift Docs

Type:   Tool

Entity Type: Tool

Entity Name: Package Manager

Date:   7 Dec 2019

Author: Herb Bowie

Index:  package
Index:  module
Index:  dependencies
Index:  tools
Index:  CocoaPods

Code: 

Body: 

My Notenik app makes use of a few third-party libraries. I had originally just downloaded the libraries I needed directly, but then started using CocoaPods. CocoaPods worked great, but then I ran across a library I wanted to try that was not set up for CocoaPods use. After some online checking, it seemed that [Swift Package Manager][spm] was now far enough along that I could use it as a dependency manager for my Mac app. So I decided to rip out CocoaPods and instead try out SPM. 

It turned out to be pretty easy. Here's how I did it. 

Step 1 was to download and run the [cocoapods-deintegrate plugin][deint]. I just followed the instructions provided in the README file. 

Next thing I did was to go over the instructions for manual removal provided in this [StackOverflow discussion][so]. There were a few things left by the deintegrate plugin, so I then threw these in the trash: 

* Podfile
* Podfile.lock
* The generated file with the '.xcworkspace' extension. 

Now I just opened my '.xcodeproj' file. 

Then, looking under the Xcode File menu, I found an entry towards the bottom for Swift Packages. I picked 'Add Package Dependency...' from that submenu, and then repeated that step for each of my primary dependencies, filling in the GitHub address for each. 

That was it! Couldn't have been easier!

[spm]: https://swift.org/package-manager/

[deint]: https://github.com/CocoaPods/cocoapods-deintegrate

[so]: https://stackoverflow.com/questions/16427421/how-to-remove-cocoapods-from-a-project
