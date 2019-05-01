---
title: "macOS Package Install"
weight: 1
---


The macOS package installer automatically installs MacPorts, [sets the shell environment](https://guide.macports.org/#installing.shell), and runs a [selfupdate](https://guide.macports.org/#using.port.selfupdate) operation to update the ports tree and MacPorts base with the latest release.

1. Download the latest {{< docs/path >}}MacPorts-2.5.4-....pkg{{< /docs/path >}} installer from the releases [on GitHub](https://github.com/macports/macports-base/releases/). Here are direct links for the latest versions of macOS:
  - __macOS 10.14 Mojave:__
      
        [MacPorts-2.5.4-10.14-Mojave.pkg](https://github.com/macports/macports-base/releases/download/v2.5.4/MacPorts-2.5.4-10.14-Mojave.pkg)
  - __macOS 10.13 High Sierra:__

        [MacPorts-2.5.4-10.13-HighSierra.pkg](https://github.com/macports/macports-base/releases/download/v2.5.4/MacPorts-2.5.4-10.13-HighSierra.pkg)
  - __macOS 10.12 Sierra:__

        [MacPorts-2.5.4-10.12-Sierra.pkg](https://github.com/macports/macports-base/releases/download/v2.5.4/MacPorts-2.5.4-10.12-Sierra.pkg)
2. Double-click the downloaded package installer to perform the default “easy” install.
3. After this step you are done already, MacPorts is now installed and your shell environment was set up automatically by the installer. To confirm the installation is working as expected, now try using {{< docs/command >}}port{{< /docs/command >}} in a _**new**_ terminal window.

{{< docs/shell-in >}}port version{{< /docs/shell-in >}}
{{< docs/shell-out >}}Version: 2.5.4{{< /docs/shell-out >}}

In case of problems such as “command not found”, make sure that you opened a new terminal window or consult [Section 2.5, “MacPorts and the Shell”](https://guide.macports.org/#installing.shell). Otherwise, please skip the remainder of this chapter and continue with [Chapter 3, Using MacPorts](https://guide.macports.org/#using) in this guide.
