Title:  Position One View within Another using Anchors

Tags:   AppKit, anchors, views

Link:   https://developer.apple.com/documentation/appkit/nsview

Text:   Apple Developer Docs

Entity Type: Class

Entity Name: NSView

Date:   21 Oct 2019

Author: Herb Bowie

Index:  anchors
Index:  views
Index:  UI layout

Code: 

// We'll use a grid view as the inner view in this example
gridView = NSGridView(views: grid)

gridView.translatesAutoresizingMaskIntoConstraints = false
parentView.addSubview(gridView!)

// Pin the grid to the edges of our main view
gridView!.leadingAnchor.constraint(equalTo: parentView.leadingAnchor, constant: 8).isActive = true
gridView!.trailingAnchor.constraint(equalTo: parentView.trailingAnchor, constant: -8).isActive = true
gridView!.topAnchor.constraint(equalTo: parentView.topAnchor, constant: 8).isActive = true
gridView!.bottomAnchor.constraint(equalTo: parentView.bottomAnchor, constant: -8).isActive = true

Body: 

Cocoa offers a number of different ways to set up your UI layouts. In many cases, you will want a flexible layout that will contract or expand along with the surrounding window, and parent view(s). 

One way to handle this is by using Anchors to position one view within another.

See the code snippet for an example. Note that the constants provide some breathing room between your subview and the parent view. Note also that you will need negative numbers for the trailing and bottom anchors in order to achieve a consistent margin around your inner view on all four sides. 
