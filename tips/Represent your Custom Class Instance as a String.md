Title:  Represent your Custom Class Instance as a String

Tags:   Swift

Link:   https://developer.apple.com/documentation/swift/customstringconvertible

Text:   Apple Developer Docs

Type:   API

Entity Type: Protocol

Entity Name: CustomStringConvertible

Date:   28 Oct 2019

Author: Herb Bowie

Code: 

// Identify the Protocol on your Class Definition
class CustomClass: CustomStringConvertible {

// Then make the String value available when requested
var description: String {
	// format the String however you would like
}

// Then other classes can retrieve the String value
customObject = CustomClass()
let str = String(describing: customObject)

Body: 

Types that conform to the CustomStringConvertible protocol can provide their own representation to be used when converting an instance to a string. The String(describing:) initializer is the preferred way to convert an instance of any type to a string. If the passed instance conforms to CustomStringConvertible, the String(describing:) initializer and the print(_:) function use the instance’s custom description property.
