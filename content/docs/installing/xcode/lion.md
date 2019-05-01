---
title: "Install Xcode on OS X 10.7 Lion or OS X 10.8 Mountain Lion"
weight: 2
---


Download the latest version of Xcode from the [Apple developer website](https://developer.apple.com/downloads/index.action) or get it using the [Mac App Store](https://itunes.apple.com/us/app/xcode/id497799835).

Xcode 4.3 and later do not automatically install the command line tools, but MacPorts requires them. To install them, open the Xcode application, go to the Preferences window, to the Downloads section, and click the Install button next to Command Line Tools. Be sure to return to this window after every Xcode upgrade to ensure that the command line tools are also upgraded.

If you wish to create Installer packages with {{< docs/command >}}port pkg{{< /docs/command >}}, you will also need to install PackageMaker, which is in the “Auxiliary Tools for Xcode” package as of Xcode 4.3. The download page for this package can be opened via the Xcode -> Open Developer Tool -> More Developer Tools... menu item. After downloading and mounting the disk image, drag the PackageMaker application to your {{< docs/path >}}/Application{{< /docs/path >}} directory.
