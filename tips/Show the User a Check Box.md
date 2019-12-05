Title:  Show the User a Check Box

Tags:   AppKit

Link:   https://developer.apple.com/documentation/appkit/nsbutton

Text:   Apple Developer Docs for NSButton

Type:   API

Entity Type: Class

Entity Name: NSButton

Index:  checkbox
Index:  UI controls

Code: 

// Define a Check Box control as a button
var tagsCkBox: NSButton!

// Create the Check Box
// Note that the combination of target and action specify what  
// class and method should be called when the user clicks on the check box
titleCkBox = NSButton(checkboxWithTitle: "Title", target: self, action: #selector(checkBoxClicked))

// Programmatically deselect the checkbox
titleCkBox.state = NSControl.StateValue.off

// Programmatically select the checkbox
titleCkBox.state = NSControl.StateValue.on

// Provide the method to be called when the user clicks
// Note that @objc needs to be prepended in order to enable 
// some special Objective-C juju
@objc func checkBoxClicked() {
	// Do something about the action
}

Body: 

A check box allows the user to check or uncheck an option. A check box is a variation of a button on macOS, and uses the NSButton class. 

See the following links for helpful info:

* [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/macos/buttons/checkboxes/)
* [Apple Documentation Archive](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/Button/Concepts/CheckBoxes.html)
* [Ray Wenderlich site](https://www.raywenderlich.com/760-macos-controls-tutorial-part-2-2)
