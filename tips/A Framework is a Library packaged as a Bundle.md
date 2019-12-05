Title:  A Framework is a Library packaged as a Bundle

Tags:   Apple

Type:   Concept

Date:   26 Sep 2019

Author: Herb Bowie

Index: framework
Index: library
Index: bundle

Body: 

On macOS frameworks are just libraries, packed into a bundle. Within the bundle you will find an actual dynamic library (libWhatever.dylib). The difference between a bare library and the framework on Mac is that a framework can contain multiple different versions of the library. It can contain extra resources (images, localized strings, XML data files, UI objects, etc.) and unless the framework is released to public, it usually contains the necessary .h files you need to use the library. 

Thus you have everything within a single package you need to use the library in your application, instead of a bunch of files to move around (a Mac bundle is just a directory on the Unix level, but the macOS treats it like a single file, pretty much like you have JAR files in Java and when you click it, you usually don't see what's inside, unless you explicitly select to show the content).

