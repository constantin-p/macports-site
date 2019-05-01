---
title: "Source Install"
weight: 2
---


If you installed MacPorts using the package installer, skip this section. To install MacPorts from the source code, follow the steps below.

1. Download and extract the [MacPorts 2.5.4 tarball](https://distfiles.macports.org/MacPorts/MacPorts-2.5.4.tar.bz2). Either do so using your browser and the Finder, or use the given commands in a terminal window.
{{< docs/shell-in >}}curl -O https://distfiles.macports.org/MacPorts/MacPorts-2.5.4.tar.bz2{{< /docs/shell-in >}}
{{< docs/shell-in >}}tar xf MacPorts-2.5.4.tar.bz2{{< /docs/shell-in >}}
2. Afterwards, perform the commands shown in the terminal window. If you wish to use a path other than {{< docs/path >}}/opt/local{{< /docs/path >}}, follow the instructions for [installing multiple copies of MacPorts](https://guide.macports.org/#installing.macports.source.multiple) instead.
{{< docs/shell-in >}}cd MacPorts-2.5.4/{{< /docs/shell-in >}}
{{< docs/shell-in >}}./configure{{< /docs/shell-in >}}
{{< docs/shell-in >}}make{{< /docs/shell-in >}}
{{< docs/shell-in >}}sudo make install{{< /docs/shell-in >}}
3. Please continue with [Section 2.5, “MacPorts and the Shell”](https://guide.macports.org/#installing.shell) to set up your shell environment.