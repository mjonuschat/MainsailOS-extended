# Klipper plugin for G-Code-based shell command execution

CustomPiOS module to install the G-Code Shell Command Extension.

After installing the extension you can execute Linux commands or even scripts
from within Klipper with custom commands defined in your printer.cfg.

## Enabling autocommit backups

The main use case for this extension is to back up your Klipper configs to GitHub.
You will need a GitHub account, a repository to be used for the backups and some
Klipper macros to make this happen.

Detailed instructions are provided by [KIAUH](https://github.com/th33xitus/kiauh/wiki/How-to-autocommit-config-changes-to-github%3F).

You can skip steps 1-3 of those instructions, these steps have been baked into
the MainsailOS image. You will need to at least do the following things:

1. Back up the initial set of files manually.
2. Push that commit to GitHub to be asked for a username & password.
3. Add a G-Code macro to your config and call it at an appropriate time during
   your print process, e.g. from your PRINT_END macro.

   A macro that should work with this setup looks like this:

   ```plain
   [gcode_shell_command backup_configs]
   command: sh /usr/local/bin/autocommit
   timeout: 60.0
   verbose: True

   [gcode_macro BACKUP_CFG]
   gcode:
        RUN_SHELL_COMMAND CMD=backup_configs
   ```

## Saving the automated printer.cfg backups

By default the printer-{date}.cfg files that are automatically created
when a file is modified through the WebUI are not backed up to the
repository. This can easily be changed by removing the following lines
from the `.gitignore` file in the `printer_data` directory:

```plain
# Moonraker auto backups
printer-[0-9]+_[0-9]+.cfg
```
