Title:  Make a Control the First Responder

Tags:   AppKit, responder

Link:   https://developer.apple.com/documentation/appkit/nswindow/1419366-makefirstresponder

Text:   Apple Developer Docs

Entity Type: Class

Entity Name: NSWindow

Date:   21 Oct 2019

Author: Herb Bowie

Index:  first responder
Index:  controls

Code: 

// First, establish an outlet for the control
@IBOutlet var searchField: NSSearchField!

// Then request the window to make this control the first responder
// This code would go in the window controller at the appropriate point
guard let confirmedWindow = self.window else { return }
confirmedWindow.makeFirstResponder(searchField)

Body: 

The first responder within a given window is also the responder (aka control) that has the focus for user input. In other words, it is the first control that will respond to user actions, including keyboard input. 
