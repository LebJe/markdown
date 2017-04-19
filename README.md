# SwiftMarkdown

[![Language](https://img.shields.io/badge/Swift-3-brightgreen.svg)](http://swift.org)
[![Build Status](https://travis-ci.org/brokenhandsio/SwiftMarkdown.svg?branch=master)](https://travis-ci.org/brokenhandsio/SwiftMarkdown)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/brokenhandsio/SwiftMarkdown/master/LICENSE)

Very simple Swift wrapper of Github's fork of [cmark](https://github.com/github/cmark). Uses a [fork](https://github.com/brokenhandsio/cmark-gfm) of cmark which has been adapted for building with SwiftPM.

# Usage

## markdown -> HTML

```swift
let markdown = "# Hello"
let html = try markdownToHTML(markdown)
print(html) //"<h1>Hello</h1>\n"
```

## Options

You can pass different options to the underlying `cmark` library. By default `safe` is passed, but this can be explicitly done with:

```swift
let html = try markdownToHTML(markdown, options: [.safe])
```

The available options are:

* sourcePosition
* hardBreaks
* safe
* noBreaks
* normalize
* validateUTF8
* smartQuotes

For more information on the available options, see [`cmark`](https://github.com/github/cmark).

# Installation

## Swift Package Manager

```swift
.Package(url: "https://github.com/brokenhandsio/SwiftMarkdown.git", majorVersion: 0, minor: 1)
```
