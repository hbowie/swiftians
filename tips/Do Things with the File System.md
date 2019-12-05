Title:  Do Things with the File System

Tags:   Foundation

Link:   https://developer.apple.com/documentation/foundation/nsfilemanager

Text:   Apple Developer Docs

Type:   API

Entity Type: Class

Entity Name: NSFileManager

Date:   28 Oct 2019

Author: Herb Bowie

Index:  file system

Code: 

do {
	try FileManager.default.removeItem(at: newURL)
	try FileManager.default.copyItem(at: oldURL, to: newURL)
} catch {
	print ("Could not Save current Collection as a new folder")
	return false
}

Body: 

Use NSFileManager for both information about, and operations on, the local file system. 

Note that you can typically use the provided singleton, named 'default', rather than creating your own.

Note also that many of the NSFileManager methods can throw errors, so you will need to use the [do-try-catch syntax] to provide the appropriate handling in the event of an error. 

[catch]: https://docs.swift.org/swift-book/LanguageGuide/ErrorHandling.html
