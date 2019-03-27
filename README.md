# Synergy: Vapor Server + Device Apps

<a id="toc"></a>
[SynergySqliteC](#linkSynergySqliteC) • 
[SynergySQLiteFramework](#linkSynergySQLiteFramework) • 
[SynergyAPI](#linkSynergyAPI) • 
[SynergyVapor](#linkSynergyVapor) • 
[Synergy Clients](#linkSynergyClients) • 
[Resources](#Resources)

It is possible to have Swift Packages which can be used on the Swift server side, and on iOS devices and in macOS applications.  The greater the separation between the views and application logic then the more the Swift Packages can be shared across the platforms. 

The `VaporExampleLabs/Synergy*` collection of packages & projects provides various working pieces of how to use a Vapor server, iOS device client and a macOS client using Swift Packages.

Each part highlights some key findings for the use of a Swift code shared in both Server backend and Client device software development.

_Note: The Synergy set of projects and packages are still a work in progress for gathering lessons learned. The goal is to create a full backend-to-client connected example sharing common swift packages._

## SynergySqliteC <a id="linkSynergySqliteC">[▴](#toc)</a>

Sometimes lower level libraries are not common between the server and device.  For example, the database Object Relationship Model (ORM) is different for Vapor and iOS/macOS have CoreData. Vapor provides Fluent. iOS/macOS provides CoreData.

This example illustrates direct use the SQLite C source code at the lowest level.

<code>[SynergySqliteC ⇗](https://github.com/VaporExamplesLab/SynergySQLiteC)</code> shows how to setup a cross platform C library into a Swift Package.

## SynergySQLiteFramework <a id="linkSynergySQLiteFramework">[▴](#toc)</a>

<code>[SynergySQLiteFramework ⇗](https://github.com/VaporExamplesLab/SynergySQLiteFramework)</code> provides a _generic_ Swift framework for using the C-base Swift Package `SynergySqliteC`.

## SynergyAPI <a id="linkSynergyAPI">[▴](#toc)</a>

<code>[SynergyAPI ⇗](https://github.com/VaporExamplesLab/SynergyAPI)</code> provides the Codable interface for the collection of Synergy applications.  Uses the generics SQLite package `SynergySQLiteFramework`.

## SynergyVapor <a id="linkSynergyVapor">[▴](#toc)</a>

<code>[SynergyVapor ⇗](https://github.com/VaporExamplesLab/SynergyVapor)</code> provides an example web application which uses the `SynergyAPI`.

## Synergy Clients <a id="linkSynergyClients">[▴](#toc)</a>

<code>[Synergy ⇗](https://github.com/VaporExamplesLab/SynergySQLiteFramework)</code> provides both an iOS and macOS client Xcode projects.  Both the iOS and macOS clients use the `SynergyAPI` package.


**Swift Packages in iOS/macOS Applications**

> Note that at this time the Package Manager has no support for iOS, watchOS, or tvOS platforms. [Source: Swift Package Manager Project](https://github.com/apple/swift-package-manager)

Even though the Swift Package manager _can not directly_ create an iOS or macOS application, Swift Packages can still be used as subprojects in the respective Xcode application projects.  

```

```

## Resources <a id="Resources">[▴](#toc)</a>

* [StackOverflow: How do I use Swift Package Manager with an existing macOS project? ⇗](https://stackoverflow.com/questions/48837369/how-do-i-use-swift-package-manager-with-an-existing-macos-project)
* [StackOverflow: Vapor server and companion iOS app examples ⇗](https://stackoverflow.com/questions/47717355/vapor-server-and-companion-ios-app-examples/48373393#comment97266087_48373393)
