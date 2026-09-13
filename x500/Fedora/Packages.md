# ARIA2
sudo yum install aria2

# Ghostty
sudo dnf copr enable scottames/ghostty
sudo dnf install ghostty

# Opencode
curl -fsSL https://opencode.ai/install | bash

# Tailscale
curl -fsSL https://tailscale.com/install.sh | sh
sudo tailscale up

# Weechat
sudo dnf install weechat

# VLC
sudo dnf install vlc
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm

sudo dnf install libavcodec-freeworld


# Zed
curl -f https://zed.dev/install.sh | sh

*Terra Repo
sudo dnf install --repofrompath 'terra,https://repos.fyralabs.com/terra$releasever' --setopt='terra.gpgkey=https://repos.fyralabs.com/terra$releasever/key.asc' terra-release

sudo dnf install zed


#ProtonVPN
wget "https://repo.protonvpn.com/fedora-$(cat /etc/fedora-release | cut -d' ' -f 3)-stable/protonvpn-stable-release/protonvpn-stable-release-1.0.4-1.noarch.rpm"

sudo dnf install ./protonvpn-stable-release-1.0.4-1.noarch.rpm && sudo dnf check-update --refresh 

sudo dnf install proton-vpn-gnome-desktop 
