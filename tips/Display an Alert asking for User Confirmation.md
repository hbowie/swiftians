Title:  Display an Alert asking for User Confirmation

Tags:   AppKit

Link:   https://developer.apple.com/documentation/appkit/nsalert

Text:   Apple Developer Docs

Type:   API

Entity Type: Class

Entity Name: NSAlert

Date:   28 Oct 2019

Author: Herb Bowie

Code: 

let alert = NSAlert()
alert.alertStyle = .warning
alert.messageText = "Really delete the Note titled '\(selectedNote!.title)'?"
// alert.informativeText = "Informative Text"

alert.addButton(withTitle: "OK")
alert.addButton(withTitle: "Cancel")
// alert.showsSuppressionButton = true
let response = alert.runModal()
if response == .alertFirstButtonReturn {
	print ("OK - Let's Delete the thing!")
} else {
	print ("Just forget the whole thing")
}

Body: 

The NSAlert class can be used to display an alert. 

See this discussion on [Stack Overflow][stack] for more useful info on this topic. 

[stack]: https://stackoverflow.com/questions/29433487/create-an-nsalert-with-swift
