Title:  Cut, Copy and Paste to and from the Clipboard

Tags:   AppKit

Type:   API

Link:   https://developer.apple.com/documentation/appkit/nspasteboard

Text:   Apple Developer Docs

Entity Type: Class

Entity Name: NSPasteboard

Date:   5 Dec 2019

Author: Herb Bowie

Index: cut
Index: copy
Index: paste
Index: clipboard
Index: pasteboard

Body: 

In my [macOS Notenik app][gh] I wanted to add the ability for the user to cut, copy and paste entire Notes using the traditional Edit menu commands and their usual keyboard shortcuts. 

Even though this seemed like a relatively simple and common thing to do, I had a rough time finding complete and current guidance on how to do this, so I thought I'd write something up to make this easier on others. 

(Note that this tip has nothing to do with [copying a custom object](copy-objects-in-swift.html), which makes use of the NSCopying protocol.)

The first thing to do is to add the following code to an appropriate point in the [responder chain](responder-chain.html). 

    /// Copy the selected item to the system clipboard.
    @IBAction func copy(_ sender: AnyObject?) {
        print("Copy an item")
    }
    
    /// Copy the selected item to the system clipboard and then
    /// attempt to delete the item.
    @IBAction func cut(_ sender: AnyObject?) {
        print("Cut an item")
    }
    
    /// Paste the passed items found in the system clipboard.
    @IBAction func paste(_ sender: AnyObject?) {
        print("Paste an item")
    } 

I added this to my NSWindowController, named 'CollectionWindowController'.

Once you add this code, then the Cut, Copy and Paste options under the Edit menu should no longer be grayed out, indicating that they are now available. 

The next trick here is storing and retrieving information from the system clipboard. 

Here's the code to paste something to the clipboard. It makes things simpler that I'm just passing a Note as a simple String (here identified as 'str'). 

    let board = NSPasteboard.general
    board.clearContents()
    board.setString(str, forType: NSPasteboard.PasteboardType.string)
    
And now here's the code to retrieve info from the clipboard. 

	let board = NSPasteboard.general
	guard let items = board.pasteboardItems else { return }
	for item in items {
		let str = item.string(forType: NSPasteboard.PasteboardType.string)
		if str != nil && str!.count > 0 {
				// Do something with the passed string.
		} // End if we found a good string
	} // end for each item

Hope others find this helpful!

[gh]: https://github.com/hbowie/notenik-swift
