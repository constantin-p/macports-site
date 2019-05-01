---
title: "Install Multiple MacPorts Copies"
weight: 4
---


Occasionally a MacPorts developer may wish to install more than one MacPorts instance on the same host. Only one copy of MacPorts may use the default prefix {{< docs/path >}}/opt/local{{< /docs/path >}}, so for additional installations use the option {{< docs/option >}}--prefix{{< /docs/option >}} as shown below. It's also recommended to change the applications dir using --with-applications-dir to avoid conflicts in {{< docs/path >}}/Applications/MacPorts{{< /docs/path >}}. Use {{< docs/option >}}--without-startupitems{{< /docs/option >}} to automatically set {{< docs/option >}}startupitem_install{{< /docs/option >}} no in the new {{< docs/path >}}macports.conf{{< /docs/path >}}, which is required to avoid conflicts in {{< docs/path >}}/Library/LaunchAgents{{< /docs/path >}} or {{< docs/path >}}/Library/LaunchDaemons{{< /docs/path >}}.


  > The first command temporarily removes the standard MacPorts binary paths because they must not be present while installing a second instance.

{{< docs/shell-in >}}export PATH=/bin:/sbin:/usr/bin:/usr/sbin{{< /docs/shell-in >}}
{{< docs/shell-in >}}MP_PREFIX=/opt/macports-test{{< /docs/shell-in >}}
{{< docs/shell-in >}}./configure --prefix=$MP_PREFIX --with-applications-dir=$MP_PREFIX/Applications --without-startupitems{{< /docs/shell-in >}}
{{< docs/shell-in >}}make{{< /docs/shell-in >}}
{{< docs/shell-in >}}sudo make install{{< /docs/shell-in >}}