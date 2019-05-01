---
title: "Uninstall"
weight: 4
---


Uninstalling MacPorts can be a drastic step, and depending on the issue you are experiencing, you may not need to do so. If you are unsure, ask on the [macports-users](https://lists.macports.org/mailman/listinfo/macports-users) mailing list first.

If you need to uninstall MacPorts, and {{< docs/command >}}port{{< /docs/command >}} is functioning, first uninstall all the installed ports by running this command in the Terminal:

{{< docs/shell-in >}}sudo port -fp uninstall installed{{< /docs/shell-in >}}

All that will be left in your installation prefix now will be files that were not registered to any port. This includes configuration files, databases, any files which MacPorts renamed in order to allow a forced installation or upgrade, and the base MacPorts software itself. You may wish to save your configuration files (most are in {{< docs/path >}}$prefix/etc{{< /docs/path >}}), databases, or any other unique data by moving it aside.

To remove all remaining traces of MacPorts, run the following command in the Terminal. If you have changed `prefix`, `applications_dir` or `frameworks_dir` from their default values, then replace {{< docs/path >}}/opt/local{{< /docs/path >}} with your prefix, replace {{< docs/path >}}/Applications/MacPorts{{< /docs/path >}} with your `applications_dir`, and/or add your `frameworks_dir` to the list, respectively.

{{< docs/shell-in >}}sudo rm -rf \
        /opt/local \
        /Applications/DarwinPorts \
        /Applications/MacPorts \
        /Library/LaunchDaemons/org.macports.* \
        /Library/Receipts/DarwinPorts*.pkg \
        /Library/Receipts/MacPorts*.pkg \
        /Library/StartupItems/DarwinPortsStartup \
        /Library/Tcl/darwinports1.0 \
        /Library/Tcl/macports1.0 \
        ~/.macports
{{< /docs/shell-in >}}

If you use a shell other than bash (perhaps tcsh), you may need to adjust the above to fit your shell's syntax. Also note that depending on which version of MacPorts you have and which ports you have installed, not all of the above paths will exist on your system. This is OK.
