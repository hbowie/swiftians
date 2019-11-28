Title:  Store and Retrieve User Preferences

Tags:   Foundation

Link:   https://developer.apple.com/documentation/foundation/userdefaults

Text:   Apple Developer Documentation

Type:   API

Entity Type: Class

Entity Name: UserDefaults

Date:   26 Sep 2019

Author: Herb Bowie

Code: 

// Get the User Defaults Singleton
let defaults = UserDefaults.standard

// Set some defaults
defaults.set(25, forKey: "Age")
defaults.set(true, forKey: "UseTouchID")
defaults.set(CGFloat.pi, forKey: "Pi")
defaults.set("Herb Bowie", forKey: "Name")
defaults.set(Date(), forKey: "LastRun")

// Now retrieve some defaults
let age = defaults.integer(forKey: "Age")

Body: 

The UserDefaults class provides a programmatic interface for interacting with the defaults system. The defaults system allows an app to customize its behavior to match a user’s preferences. For example, you can allow users to specify their preferred units of measurement or media playback speed. Apps store these preferences by assigning values to a set of parameters in a user’s defaults database. The parameters are referred to as defaults because they’re commonly used to determine an app’s default state at startup or the way it acts by default.

Note that not all of the getters return optional values when no value can be found for the indicated key. Getters that return numeric values tend to return zeroes, and the boolean getter returns false when the key can't be found.  

Additional link:

* [Hacking with Swift](https://www.hackingwithswift.com/read/12/2/reading-and-writing-basics-userdefaults)
