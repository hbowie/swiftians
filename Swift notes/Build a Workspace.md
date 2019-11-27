Title:  Build a Workspace

Tags:   Xcode

Link:   https://medium.com/@OddNetworks/using-xcode-workspaces-to-develop-with-the-oddsdk-ee4c0931b30e

Text:   Odd Networks on Medium

Type:   Xcode Action

Date:   26 Sep 2019

Author: Herb Bowie

Body: 

A workspace is a way of combining multiple projects into a single work area. This is especially useful with projects that are dependent on one another. 

A workspace is stored on disk as a single file with the extension .xcworkspace. That file can be stored anywhere outside of the projects to be included in the workspace. When you open that file in Xcode (say, by double-clicking on it), then all of the projects in that workspace will open at the same time and all be accessible through a single window. 

Before creating a workspace, you should close any projects that you want to include in the workspace. 

After creating a new workspace, you should click the plus sign in the lower left corner of your project navigator, then add the .xcodeproj file for one of your projects. Repeat this step for each project you wish to have included in the workspace. 

Use the File / New Menu command to create a new Workspace. 

Also see this article in the Apple Developer Archive:

* [Xcode Workspace](https://developer.apple.com/library/archive/featuredarticles/XcodeConcepts/Concept-Workspace.html)


