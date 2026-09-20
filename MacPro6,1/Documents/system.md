
# Broadcom
yay -S b43-fwcutter

# 1. Install the appropriate kernel headers
sudo pacman -Syu linux-headers

# 2. Install the DKMS Broadcom driver package
sudo pacman -S broadcom-wl-dkms


- Unload conflicting kernel modules:
sudo modprobe -r b43 b44 b43legacy ssb brcmsmac bcma wl

- Load the correct driver:
sudo modprobe wl

- Verify the interface is visible:
ip link show

# 3. Persistent Blacklisting (Preventing Future Conflicts)
sudo nano /etc/modprobe.d/broadcom-wl.conf

- Add this and save
blacklist b43
blacklist b44
blacklist b43legacy
blacklist ssb
blacklist brcmsmac
blacklist bcma

# Fan
yay -S macfanctld

# NTFS
sudo pacman -S nfs-utils ntfs-3g

Optional dependencies for ntfs-3g
    ntfsprogs: userspace utilities
    
# Reflector
 pacman -S reflector
 
sudo reflector --latest 10 --protocol https --sort rate --save /etc/pacman.d/mirrorlist
