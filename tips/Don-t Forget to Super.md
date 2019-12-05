Title:  Don't Forget to Super

Tags:   Swift

Link:   https://docs.swift.org/swift-book/LanguageGuide/Inheritance.html

Text:   The Swift Programming Language

Index:  super
Index:  errors

Body: 

When overriding a function provided by an API, don't forget to insert a super call to the API being overridden, unless you are sure you want to completely dispense with whatever functionality is provided by the overridden class. 

A failure to add a super call will not be flagged by Xcode, and will often cause problems, if it is done unintentionally or forgetfully. 
