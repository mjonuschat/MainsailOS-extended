# passwordless-sudo

This module re-enables the passwordless `sudo` functionality for the __pi__ user.

Please be mindful of the security implications this has, the intended use case
is for installing KlipperScreen and other user-specific applications after
`password-for-sudo` has been run.

The best practice is to use this module early in the build process and add
`password-for-sudo` as the final module in the boot process.