---
title: "Git Install"
weight: 3
---


If you installed MacPorts using the package installer, skip this section.

There are times when some may want to run MacPorts from a version newer than the current stable release. Maybe there's a new feature that you'd like to use, or it fixes an issue you've encountered, or you just like to be on the cutting edge. These steps explain how to setup MacPorts for developers, using only Git to keep MacPorts up to date.

Though a distinction is made between pre-release and release versions of MacPorts base, the ports collection supports no such distinction or versioning. The [selfupdate](https://guide.macports.org/#using.port.selfupdate) command installs the latest ports tree, and updates MacPorts base to the latest released version.

1. Check out MacPorts source

    Pick a location to store a working copy of the MacPorts code. For this example, {{< docs/path >}}/opt/mports{{< /docs/path >}} will be used, but you can put the source anywhere. This example will create {{< docs/path >}}/opt/mports/macports-base{{< /docs/path >}} containing everything needed for MacPorts.
{{< docs/shell-in >}}mkdir -p /opt/mports{{< /docs/shell-in >}}
{{< docs/shell-in >}}cd /opt/mports{{< /docs/shell-in >}}
{{< docs/shell-in >}}git clone https://github.com/macports/macports-base.git{{< /docs/shell-in >}}
{{< docs/shell-in >}}git checkout v2.5.4  # skip this if you want to use the development version{{< /docs/shell-in >}}
2. Build and Install MacPorts
    
    MacPorts uses autoconf and makefiles for installation. These commands will build and install MacPorts to {{< docs/path >}}/opt/local{{< /docs/path >}}. You can add {{< docs/option >}}--prefix{{< /docs/option >}} to {{< docs/path >}}./configure{{< /docs/path >}} to relocate MacPorts to another directory if needed.
{{< docs/shell-in >}}cd /opt/mports/macports-base{{< /docs/shell-in >}}
{{< docs/shell-in >}}./configure --enable-readline{{< /docs/shell-in >}}
{{< docs/shell-in >}}make{{< /docs/shell-in >}}
{{< docs/shell-in >}}sudo make install{{< /docs/shell-in >}}
{{< docs/shell-in >}}make distclean{{< /docs/shell-in >}}
3. (Optional) Configure MacPorts to use port information from Git

    This step is useful if you want to do port development. Check out the ports tree from git:
{{< docs/shell-in >}}cd /opt/mports{{< /docs/shell-in >}}
{{< docs/shell-in >}}git clone https://github.com/macports/macports-ports.git{{< /docs/shell-in >}}
  
    Then open {{< docs/path >}}/opt/local/etc/macports/sources.conf{{< /docs/path >}} in a text editor. The last line should look like this:    
{{< docs/shell-in >}}rsync://rsync.macports.org/macports/release/tarballs/ports.tar [default]{{< /docs/shell-in >}}

    Change it to point to the working copy you checked out:
{{< docs/shell-in >}}file:///opt/mports/macports-ports [default]{{< /docs/shell-in >}}
4. Environment

    You should setup your PATH and other environment options according to [Section 2.5, “MacPorts and the Shell”](https://guide.macports.org/#installing.shell).
