Title:  Obtain Information About a File

Tags:   Foundation, file

Link:   https://developer.apple.com/documentation/foundation/filemanager/1410452-attributesofitem

Text:   Apple Developer Docs

Entity Type: Class

Entity Name: FileManager

Date:   21 Oct 2019

Author: Herb Bowie

Code: 

let fileManager = FileManager.default
do {
	let attributes = try fileManager.attributesOfItem(atPath: noteURL.path)
	let creationDate = attributes[FileAttributeKey.creationDate]
	let lastModDate = attributes[FileAttributeKey.modificationDate]
	print("Creation Date = \(creationDate)")
	print("Last Mod Date = \(lastModDate)")
}
catch let error as NSError {
	print("Ooops! Something went wrong: \(error)")
}


Body: 

See Code Snippet. 

Also see the [Apple Developer Docs for FileAttributeKey](https://developer.apple.com/documentation/foundation/fileattributekey).

