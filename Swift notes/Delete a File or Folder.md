Title:  Delete a File or Folder

Tags:   Foundation, files

Link:   https://developer.apple.com/documentation/foundation/nsfilemanager

Text:   Apple Developer Docs

Entity Type: Class

Entity Name: NSFileManager

Date:   21 Oct 2019

Author: Herb Bowie

Code: 

// Delete an item immediately
do {
	try FileManager.default.removeItem(at: newURL)
} catch {
	print("Could not delete the thing")
}

// Move an item to the trash
do {
	try FileManager.default.trashItem(at: oldURL, resultingItemURL: nil)
} catch {
	print("Could not trash the item at \(oldURL.path)")
}


Body: 

You can use the NSFileManager.default singleton to delete a file or folder, but you should be aware that there are two different options here.

- Use removeItemAtURL or removeItemAtPath to delete an item immediately;
- Use trashItemAtURL to move an item to the trash, where the user can find and retrieve it, if necessary. (However, starting in Catalina, this seems to run into permissions problems.)

Both will need to be wrapped in do-try-catch blocks. 

