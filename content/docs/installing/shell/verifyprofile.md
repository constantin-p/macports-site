---
title: "Verify the Configuration File"
weight: 2
---


To verify that the file containing the MacPorts variables is in effect, type {{< docs/command >}}env{{< /docs/command >}} in the terminal to verify the current environment settings after the file has been created. Example output for {{< docs/command >}}env{{< /docs/command >}} is shown below.

  > Changes to shell configuration files do not take effect until a new terminal session is opened.

{{< docs/shell-out >}}MANPATH=
TERM_PROGRAM=Apple_Terminal
TERM=xterm-color
SHELL=/bin/bash
TERM_PROGRAM_VERSION=237
USER=joebob
__CF_USER_TEXT_ENCODING=0x1FC:0:0
PATH=/opt/local/bin:/opt/local/sbin:/bin:/sbin:/usr/bin:/usr/sbin
PWD=/Users/joebob
EDITOR=/usr/bin/pico
SHLVL=1
HOME=/Users/joebob
LOGNAME=joebob
DISPLAY=:0.0
SECURITYSESSIONID=b0cea0
_=/usr/bin/env
{{< /docs/shell-out >}}
