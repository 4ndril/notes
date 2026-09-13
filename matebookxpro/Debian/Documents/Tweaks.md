# Tweak the Shell Experience

nano ~/.bashrc

alias ll='ls -alF'
alias update='sudo apt update && sudo apt upgrade -y'
alias cleanup='sudo apt autoremove && sudo apt autoclean'
alias gs='git status'
alias serve='python3 -m http.server 8000'

# Optimize Power and Performance (Especially on Laptops)
sudo apt install tlp tlp-rdw
sudo systemctl enable tlp

# Synaptic
sudo apt install synaptic -y
