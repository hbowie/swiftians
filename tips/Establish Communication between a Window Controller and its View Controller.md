Title:  Establish Communication between a Window Controller and its View Controller

Tags:   AppKit

Link:   https://developer.apple.com/documentation/appkit/nswindowcontroller

Text:   Apple Developer Docs

Entity Type: Class

Entity Name: NSWindowController

Date:   21 Oct 2019

Author: Herb Bowie

Index:  window
Index:  view
Index:  controller

Code: 

guard let vc = customWindowController.contentViewController as? CustomViewController else { return }
vc.window = customWindowController

Body: 

A View Controller doesn't seem to have any built-in way to communicate with its window controller. 

On the other hand, a Window Controller can identify its Content View Controller. 
