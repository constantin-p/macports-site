---
title: "MacPorts and the Shell"
weight: 5
---


MacPorts requires that some environment variables be set in the shell. When MacPorts is installed using the macOS package installer, a “postflight” script is run after installation that automatically adds or modifies a shell configuration file in your home directory, ensuring that it defines variables according to the rules described in the following section. Those [installing MacPorts from source code](https://guide.macports.org/#installing.macports.source) must modify their environment manually using the rules as a guide.

Depending on your shell and which configuration files already exist, the installer may use {{< docs/path >}}.profile{{< /docs/path >}}, {{< docs/path >}}.bash_login{{< /docs/path >}}, {{< docs/path >}}.bash_profile{{< /docs/path >}}, {{< docs/path >}}.tcshrc{{< /docs/path >}}, or {{< docs/path >}}.cshrc{{< /docs/path >}}.
