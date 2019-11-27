Title:  Create a Scrolling Text View

Tags:   AppKit

Link:   https://developer.apple.com/documentation/appkit/nsscrollview

Text:   Apple Developer Docs for NSScrollView

Type:   API

Entity Type: Class

Entity Name: NSScrollView & NSTextView

Code: 

// Define the views
var scrollView: NSScrollView!
var textView: NSTextView!

// Set up the Scroll View
let scrollRect = NSRect(x: 0, y: 0, width: 300, height: 150)
scrollView = NSScrollView(frame: scrollRect)
scrollView.hasVerticalScroller = true
scrollView.hasHorizontalScroller = false
scrollView.autoresizingMask = [.width, .height]

// Set up the Text View
let contentSize = scrollView.contentSize
let textRect = NSRect(x: 0, y: 0, width: contentSize.width, height: contentSize.height)
textView = NSTextView(frame: textRect)
textView.minSize = NSSize(width: 0, height: contentSize.height)
textView.maxSize = NSSize(width: 32000, height: 32000)
textView.isVerticallyResizable = true
textView.isHorizontallyResizable = false
textView.autoresizingMask = .width
textView.textContainer!.containerSize = NSSize(width: contentSize.width, height: 32000)
textView.textContainer!.widthTracksTextView = true

// Add the Text View to the Scroll View
scrollView.documentView = textView

Body: 

A scrolling text view is commonly required in applications, and Interface Builder provides an NSTextView configured just for this purpose. However, at times you may need to create a scrolling text view programmatically.

See the [Apple Documentation Archive][archive] for more useful info on this topic. 

[archive]: https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/TextUILayer/Tasks/TextInScrollView.html
