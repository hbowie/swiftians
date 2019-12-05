Title:  Copy Objects in Swift

Tags:   Swift

Type:   API

Entity Type: Protocol

Entity Name: NSCopying

Date:   28 Oct 2019

Author: Herb Bowie

Index:  copy

Code: 

// Conform to NSCopying
class CustomClass: NSCopying {

// Implement the Copy method
func copy(with zone: NSZone? = nil) -> Any {
    // Create your new object, copy data to it, and return it
}

// Now copy at will
let twin = originalObject.copy() as! CustomClass

Body: 

Here's how to copy an object in Swift. 

1. Have your custom class conform to the NSCopying protocol. 

2. Implement the 'copy(with:)' method in your custom class. 

3. Call 'copy()' on your object. 
