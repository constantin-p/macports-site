---
title: "Getting Started"
date: 2019-04-30T10:52:53+02:00
draft: false
---

## Quickstart

1. Install [Xcode and the Xcode Command Line Tools](https://guide.macports.org/#installing.xcode)
2. Agree to Xcode license in Terminal: `sudo xcodebuild -license`
3. Install MacPorts for your version of the Mac operating system:
  - [macOS Mojave v10.14](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.14-Mojave.pkg)
  - [macOS High Sierra v10.13](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.13-HighSierra.pkg)
  - [macOS Sierra v10.12](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.12-Sierra.pkg)
  - [OS X El Capitan v10.11](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.11-ElCapitan.pkg)
  - [Older OS? See here](https://www.macports.org/install.php#installing)


## Installing MacPorts

MacPorts version 2.5.4 is available in various formats for download and installation (note, if you are upgrading to a new major release of macOS, see the [migration info page](https://trac.macports.org/wiki/Migration)):

- “pkg” installers for [Mojave](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.14-Mojave.pkg), [High Sierra](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.13-HighSierra.pkg), [Sierra](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.12-Sierra.pkg) and [El Capitan](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.11-ElCapitan.pkg), for use with the macOS Installer. This is the simplest installation procedure that most users should [follow](https://www.macports.org/install.php#pkg) after meeting the requirements listed [below](https://www.macports.org/install.php#requirements). Installers for legacy platforms [Yosemite](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.10-Yosemite.pkg), [Mavericks](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.9-Mavericks.pkg), [Mountain Lion](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.8-MountainLion.pkg), [Lion](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.7-Lion.pkg), [Snow Leopard](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.6-SnowLeopard.pkg), [Leopard](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.5-Leopard.dmg) and [Tiger](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4-10.4-Tiger.dmg) are also available.

TODO

Checksums for our packaged [downloads](https://distfiles.macports.org/MacPorts/) are contained in the corresponding [checksums file](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4.chk.txt).

Please note that in order to install and run MacPorts on macOS, your system must have installations of the following components:

1. Apple's [Xcode](https://developer.apple.com/technologies/tools/) Developer Tools (version 10.0 or later for Mojave, 9.0 or later for High Sierra, 8.0 or later for Sierra, 7.0 or later for El Capitan, 6.1 or later for Yosemite, 5.0.1 or later for Mavericks, 4.4 or later for Mountain Lion, 4.1 or later for Lion, 3.2 or later for Snow Leopard, or 3.1 or later for Leopard), found at the [Apple Developer](https://developer.apple.com/downloads/) site, on your Mac operating system installation CDs/DVD, or in the Mac App Store. Using the latest available version that will run on your OS is highly recommended, except for Snow Leopard where the last free version, 3.2.6, is recommended.
2. Apple's Command Line Developer Tools can be installed on recent OS versions by running this command in the Terminal:<br/>```xcode-select --install```<br/>Older versions are found at the Apple Developer site, or they can be installed from within Xcode back to version 4. Users of Xcode 3 or earlier can install them by ensuring that the appropriate option(s) are selected at the time of Xcode's install ("UNIX Development", "System Tools", "Command Line Tools", or "Command Line Support").
3. Xcode 4 and later users need to first accept the Xcode EULA by either launching Xcode or running:<br/>```xcodebuild -license```
4. (Optional) The X11 windowing environment for ports that depend on the functionality it provides to run. You have multiple choices for an X11 server:
  - Install the xorg-server port from MacPorts.
  - The [XQuartz Project](https://www.xquartz.org/) provides a complete X11 release for macOS including server and client libraries and applications.
  - Apple's X11.app is provided by the “X11 User” package on older OS versions. It is always installed on Lion, and is an optional installation on your system CDs/DVD with previous OS versions.


### macOS Package (.pkg) Installer

TODO


### Source Installation

TODO


### Git Sources

TODO


### Selfupdate

TODO


### Other Platforms

TODO


### Help

TODO

