---
title: "Introduction"
weight: 1
---


MacPorts is an easy to use system for compiling, installing, and managing open source software. MacPorts may be conceptually divided into two main parts: the infrastructure, known as MacPorts base, and the set of available ports.

A MacPorts port is a set of specifications contained in a [Portfile](https://guide.macports.org/#development.introduction) that defines an application, its characteristics, and any files or special instructions required to install it. This allows you to use a single command to tell MacPorts to automatically download, compile, and install applications and libraries. But using MacPorts to manage your open source software provides several other significant advantages.

For example, MacPorts:

- Installs automatically any required support software, known as [dependencies](https://guide.macports.org/#reference.dependencies), for a given port.
- Provides for uninstalls and upgrades for installed ports.
- Confines ported software to a private “sandbox” that keeps it from intermingling with your operating system and its vendor-supplied software to prevent them from becoming corrupted.
- Allows you to create pre-compiled binary installers of ported applications to quickly install software on remote computers without compiling from source code.

MacPorts is developed on macOS, though it is designed to be portable so it can work on other Unix-like systems, especially those descended from the Berkeley Software Distribution (BSD). In practice, installing ports only works on macOS. MacPorts base can be compiled on Linux (and possibly other POSIX-compatible systems) where it is mainly used to set up mirrors and generate support files for installations on macOS.

The following notational conventions are used in the MacPorts Guide to distinguish between terminal input/output, file text, and other special text types.

- Terminal I/O and file text:
{{< docs/shell-in >}}Commands to be typed into a terminal window.{{< /docs/shell-in >}}
{{< docs/shell-out >}}Command output to a terminal window.{{< /docs/shell-out >}}
{{< docs/shell-content >}}File text.{{< /docs/shell-content >}}

- Other special text types:
  - A hyperlink: [spontaneous combustion](https://en.wikipedia.org/wiki/Spontaneous_combustion).
  - A file: {{< docs/path >}}/var/log/system.log{{< /docs/path >}}.
  - A command: {{< docs/command >}}ifconfig{{< /docs/command >}}.
  - An option: port {{< docs/option >}}install{{< /docs/option >}}.
