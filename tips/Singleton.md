Title:  Singleton

Tags:   Swift

Link:   https://medium.com/@nimjea/singleton-class-in-swift-17eef2d01d88

Text:   Anand Nimje on Medium

Code: 

// A class following the singleton pattern. 
class MasterCollection {
    
	/// Provide a standard shared singleton instance
	static let shared = MasterCollection()

	/// Private initializer to enforce usage of the singleton instance
	private init() {
	}

	func doSomething() {

	}

}

	// Then, in other classes, you can do this:
	MasterCollection.shared.doSomething()

	// Alternatively, you can use shorthand in your code
	let master = MasterCollection.shared

	master.doSomething()

Body: 

The singleton pattern is a software design pattern that restricts the instantiation of a class to one single instance. This is useful when exactly one object is needed to coordinate actions across a system. Apple makes use of the singleton pattern for the FileManager and UserDefaults classes, as examples. But the Swift language makes it easy for you to write your own singletons as well. 

Note that the single static instance of a singleton class is usually named 'shared' or 'standard' or 'default'. 
