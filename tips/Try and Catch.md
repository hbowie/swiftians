Title:  Try and Catch

Tags:   Swift

Link:   https://docs.swift.org/swift-book/LanguageGuide/ErrorHandling.html

Text:   Swift Docs

Type:   Language Syntax

Date:   28 Oct 2019

Author: Herb Bowie

Index:  do
Index:  try
Index:  catch
Index:  errors

Code: 

do {
	try FileManager.default.removeItem(at: newURL)
	try FileManager.default.copyItem(at: oldURL, to: newURL)
} catch {
	print ("Could not Save current Collection as a new folder")
	return false
}

Body: 

In order to call a method that might raise an error, you will need to do the following:

1. Precede one or more trys with a do;

2. Try to execute one or more method calls

3. Catch any errors that might have occurred. 

See code snippet for an example. 
