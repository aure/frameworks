# Highly Desirable Frameworks

This repository is here to support updates to the following checklist and also contains materials from a companion presentation.

This checklist can be used as a starting point to evaluate a framework's quality.  It is intended to be used by potential consumers of frameworks as well as developers of frameworks who want to make sure they've covered all the basics.

It was heavily influenced, inspired by, and cribbed from [The POSSIBLE Mobile Seaworthy Framework Checklist for Vendors](https://gist.github.com/POMBuilds/eb439cfa2300b080c7b75006ab69265e).  The biggest difference between this list and that one is that this focuses on things that are noticeable quickly when a potential user comes across a framework.  Hence, detailed items like code quality are left to much longer discussions (and even textbooks)!

This checklist is not an all or nothing affair - if a framework satisfies 85% of the items below that is pretty good.  In some cases, the rules below need to be broken and that is fine.

There are several sections to this document so you may want to skip ahead:

* [README](#README)
* [Community Engagement](#Community Engagement)
* [Sample Projects](#SampleProjects)

<a name="README"></a>
## README

The README is often the very first look that a potential will be judging a framework by so it can be the start of a love-at-first-sight relationship or immediately off-putting.  

### Use Shields/Badges from [Shields.io](https://shields.io/)

Badges along the top of the README gives an experienced reader the ability to quickly assess basic aspects of the framework.

* Tests / Build Status
* License
* Package Manager Compatibility (Carthage, Cocoapods)

### Introduce the Framework

* State the problem it solves and summarize how it solves it
* Show off a little tase of what makes it so cool

### Installation and Integration Instructions

Guide the user through the supported integration methods

* CocoaPods
* Carthage
* Swift Package Manager
* Manual

Here the developer should also provide a list of bundled third-party libraries used in the framework so that potential users can assess compatibility with other third-party frameworks.

### Details

* Credits
* License Information

### Don'ts

* Don't use the README as a change log
* Don't use the README to include the full text of your license

<a name="CommunityEngagement"></a>
## Community

* An actively managed Github Issue Tracker

The number of issues ideally is small, but for big projects, there can be many, just make sure they are being responded to and a majority are closed.

* Very actively managed Pull Requests

The number of pull requests should be zero or near to zero.  A pull request is usually someone's legitimate attempt at improving the framework and it should at least be addressed with some responses if not action.  If the pull request was made by a misguided person, that is also readily closeable.  The only open pull requests should be good ideas with flawed but salvageable implementations.

If there are open pull requests, they're a good place to check for continuous integration.  If the pull request has tests that are shown to fail, that is a good reason why it hasn't been accepted yet.

* Use of the Github Projects feature

This is one of the newest Github features, so it might be empty, but if it is not, that is a good sign the developer is actively engaging the community in a meaningful way.

* Pulse and Graphs

Just to cover the remaining Github header items, these can be used to validate activity on a framework, but we can't think of anything we'd see here that would necessarily be a red flag.


<a name="SampleProjects"></a>
## Sample Projects

A framework should provide at least one sample project that satisfies as much of the following checklist as possible.

* Sample projects should build cleanly and run on the simulator or a device with zero issues or warnings
* Sample projects should be part of the continuous integration process
* Sample projects for iOS should be universal (iPhone, iPad)
* Sample projects do not require third-party tools such as Cocoapods

Bonus points for:

* More than one sample project
* Sample projects written in both Objective-C and Swift

<a name="Technical"></a>

## First-build Gotchas

* Release versions of the framework were built for the latest non-beta version of Xcode

* The framework provides configurable debug log levels with the option to completely silence them.

* The framework has a small memory and on-disk footprint, or is configurable to be slimmer.

* The framework has been tested with all of the deployment targets supported.

* The framework supports Bitcode and can build with Bitcode enabled.

* If the framework includes a Universal binary, the provided fat binary must have the architectures needed (run lipo -info on the binary from Terminal to see what architectures it supports): arm64, armv7, i386, x86_64.

## Documentation beyond the README

* The framework's public interfaces are commented with [Headerdoc](http://nshipster.com/swift-documentation/).

* The framework's public interfaces use Objective-C nullability tags and typed collection syntax.

* The SDK package provides comprehensive documentation that describes SDK setup and use.

## Releases

* Branches should be created for beta OS versions or Swift Language changes.  (Swift3 was a big change that required a lot of new development).

