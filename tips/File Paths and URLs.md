Title:  File Paths and URLs

Tags:   Foundation, file, path, url

Link:   https://developer.apple.com/documentation/foundation/url

Text:   Apple Developer Docs

Entity Type: Class

Entity Name: URL

Author: Herb Bowie

Code: 

// Let's start with a URL we got back from NSOpenPanel or something like that
guard let urlOne = openPanel.url else { return }

// Now let's get the path representation
let path = urlOne.path
// path == "/Users/hbowie/Dropbox"

// Now let's get the full URL representation
let urlString = urlOne.absoluteString
// urlString == "file:///Users/hbowie/Dropbox"

let urlTwo = URL(fileURLWithPath: path)
// Now urlTwo == urlOne

let urlThree = URL(urlString)
// Now urlThree == urlOne

let urlFour = URL(path)
// urlFour == nil


Body: 

It's good to keep in mind that you can actually point to a file or folder programmatically in three distinct ways:

1. A URL
2. A String containing a file path -- typically starting with a forward slash to indicate the system root. 
3. A String representation of a URL pointing to the file location, typically starting with 'file:///'.

(And this is not even counting relative paths or path components!)

See the code snippets for examples of how to convert back and forth between these representations. 

