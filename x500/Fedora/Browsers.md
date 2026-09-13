#Zen
sudo dnf copr enable firminunderscore/zen-browser

sudo dnf install zen-browser

curl -fsSL https://github.com/zen-browser/updates-server/raw/refs/heads/main/install.sh | $SHELL

#Tor
https://www.torproject.org/download/
cd ~/Downloads
tar -xf tor-browser-linux-x86_64-15.0.19.tar.xz
cd tor-browser
./start-tor-browser.desktop --register-app

