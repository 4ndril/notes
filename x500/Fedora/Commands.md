#Installing and Removing
sudo dnf install <package>: Installs a new software package.
sudo dnf remove <package>: Deletes an installed package.
sudo dnf autoremove: Cleans up unused leftover dependency files.

#Upgrading and Updates
dnf check-update: Checks if any package updates are available without installing them.
sudo dnf upgrade: Upgrades all system packages to their latest versions.
sudo dnf upgrade <package>: Updates only one specific package.

#Searching and Listing
dnf search <keyword>: Looks for packages matching a keyword.
dnf list --installed: Shows a list of all packages currently installed on your system.
dnf info <package>: Displays details and descriptions for a package.
