---
title: "Override Xresources"
weight: 1
description: >
  Learn how to stage user copies of Regolith configuration files.
---

Regolith relies on the Xresource system to provide a consolidated interface configuration.  By changing Xresource values, Regolith can be customized in ways such as updating the user interface, specifying custom behaviors, or defining a specific format for the clock.

## Determining what values can be changed

The `xrdb` tool can be used to list the existing Xresource values.  See [here for a table of existing values](../../reference/xresources) in the R1.3.1 release.


## Example - Update the UI for High DPI Screens
1. Create or add the following value to your `~/.config/regolith/Xresources` file:
```bash
Xft.dpi: 192
```
2. Reload the Xresource configuration:
```bash
$ regolith-look refresh
```
3. Open a new terminal to see the change take effect.

<sub>192 is just an example value, please adjust as needed.</sub>

{{% pageinfo %}}
Regolith generates many of these values from a canonical set of definitions.  See [this readme](https://github.com/regolith-linux/regolith-styles) for more details.  If you find yourself updating many values, it may be more concise to create your own look instead.
{{% /pageinfo %}}