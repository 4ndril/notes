#  Add yourself to sudoers group
su -
usermod -aG sudo your_username

# Update and upgrade system
sudo apt --update upgrade


# Change sources to more readable format 
sudo nano /etc/apt/sources.list

- Then, add a # at the beginning of every line.
- Create new file in /etc/apt/sources.list.d/debian.sources. And put:

Types: deb deb-src
URIs: https://deb.debian.org/debian
Suites: trixie trixie-updates
Components: main contrib non-free non-free-firmware
Enabled: yes
Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg

Types: deb deb-src
URIs: https://security.debian.org/debian-security
Suites: trixie-security
Components: main contrib non-free non-free-firmware
Enabled: yes
Signed-By: /usr/share/keyrings/debian-archive-keyring.gpg

sudo apt --update upgrade


# Install Nvidia drivers
sudo apt install linux-headers-amd64

sudo apt install nvidia-kernel-dkms nvidia-driver firmware-misc-nonfree

- Newer cards 
sudo apt install nvidia-open-kernel-dkms nvidia-driver firmware-misc-nonfree

