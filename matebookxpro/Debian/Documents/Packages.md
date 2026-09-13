# Essential Packages
sudo apt install curl wget vim git htop rsync vlc p7zip-full

# Ghostty
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/mkasberg/ghostty-ubuntu/HEAD/install.sh)"

# ProtonVPN


# Synaptic
sudo apt install synaptic -y

# Tailscale
curl -fsSL https://tailscale.com/install.sh | sh
sudo tailscale up
sudo systemctl enable --now tailscaled

# Opencode
curl -fsSL https://opencode.ai/install | bash


# Zed
curl -f https://zed.dev/install.sh | sh


