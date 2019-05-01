---
title: "The Postflight Script"
weight: 1
---


The postflight script automatically sets the `PATH` variable, and optionally the `MANPATH` and `DISPLAY` variables according to the rules described below. If a current shell configuration file exists at installation time it is renamed to “mpsaved_$timestamp”. Those i[nstalling MacPorts from source code](https://guide.macports.org/#installing.macports.source) must modify their environment manually using the rules as a guide.

- Required: `PATH` variable

    This variable is set by the postflight script to prepend the MacPorts executable paths to the current path as shown. This puts the MacPorts paths at the front of `PATH` so that the MacPorts binaries will take precedence over vendor-supplied binaries.
{{< docs/shell-content >}}export PATH=/opt/local/bin:/opt/local/sbin:$PATH{{< /docs/shell-content >}}
  
  > The user environment's `$PATH` is not in effect while ports are being installed, because the `$PATH` is scrubbed before ports are installed, and restored afterwards. To change the search path for locating system executables (rsync, tar, etc.) during port installation, see the [macports.conf](https://guide.macports.org/#internals.configuration-files.macports-conf) file variable binpath. But changing this variable is for advanced users only, and is not generally needed or recommended.

- Optional: `MANPATH` variable

    Condition: If prior to MacPorts installation a `MANPATH` variable exists in a current {{< docs/path >}}.profile{{< /docs/path >}} that contains neither the value {{< docs/path >}}${prefix}/share/man{{< /docs/path >}}, nor any empty items separated by a colon, the postflight script sets the `MANPATH` variable as shown below. Otherwise, the `MANPATH` variable is omitted.

- Optional: `DISPLAY` variable

    Condition: If installing on a Mac OS X version earlier than 10.5 (Leopard), and if a shell configuration file exists at time of MacPorts installation without a `DISPLAY` variable, the postflight script sets a `DISPLAY` variable as shown below. The `DISPLAY` variable is always omitted on Mac OS X 10.5 or higher.
{{< docs/shell-content >}}export DISPLAY=:0.0{{< /docs/shell-content >}}
