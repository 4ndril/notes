# Zen Browser
curl -fsSL https://github.com/zen-browser/updates-server/raw/refs/heads/main/install.sh | $SHELL

# Tor Browser
Go to https://www.torproject.org/download/

-Open your terminal and move to your downloads folder using:
cd ~/Downloads

-Extract the compressed archive with the command:
tar -x -f <downloaded-file-name.tar.xz> (replace with your exact file name).

-Change into the newly extracted directory:
cd tor-browser (or the specific folder name created).

-Register and run the desktop application script so it integrates smoothly with your system:
./start-tor-browser.desktop --register-app
