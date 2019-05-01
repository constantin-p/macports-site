---
title: "Optional Editor Variables"
weight: 3
---


You can set an environment variable in order to use your favorite text editor with the {{< docs/command >}}port{{< /docs/command >}} edit command.

MacPorts will check `MP_EDITOR`, `VISUAL` and `EDITOR` in this order, allowing you to either use a default editor shared with other programs (`VISUAL` and `EDITOR`) or a MacPorts-specific one (`MP_EDITOR).

For example, to use the nano editor, add this line to your bash config:

{{< docs/shell-content >}}export EDITOR=/usr/bin/nano{{< /docs/shell-content >}}

To use the user-friendly GUI editor [BBEdit](https://www.barebones.com/products/bbedit/) (installation required), add this line:

{{< docs/shell-content >}}export EDITOR=/Applications/BBEdit.app/Contents/Helpers/bbedit_tool{{< /docs/shell-content >}}

To keep a command-line text editor as default while using BBEdit with portfiles, add this:

{{< docs/shell-content >}}export EDITOR=/usr/bin/vi{{< /docs/shell-content >}}
{{< docs/shell-content >}}export MP_EDITOR=/Applications/BBEdit.app/Contents/Helpers/bbedit_tool{{< /docs/shell-content >}}
