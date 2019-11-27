Title:  Computed Properties

Tags:   Swift

Link:   https://docs.swift.org/swift-book/LanguageGuide/Properties.html

Text:   Swift Docs

Type:   Language Syntax

Date:   28 Oct 2019

Author: Herb Bowie

Code: 

// Full Syntax for a computed property
var someProperty: String {
	get {
		// Return the computed property
		return "some property"
	}
	set(newProperty) {
		// Save the new value or transform it or something
		var savedProperty = newProperty
	}
}

// You can omit an explicit name for the new value in the setter
var someProperty: String {
	get {
		// Return the computed property
		return "some property"
	}
	set(newProperty) {
		// Save the new value or transform it or something
		var savedProperty = newProperty
	}
}

// Or supply the getter without a setter using shorthand
var someProperty: String {
	// Return the computed property
	return "some property"
}

// Unlike Java, invocation of the getters and setters is implicit
someString = someObject.someProperty
someObject.someProperty = "A new value for the property"

Body: 

In addition to stored properties, classes, structures, and enumerations can define computed properties, which do not actually store a value. Instead, they provide a getter and an optional setter to retrieve and set other properties and values indirectly.
