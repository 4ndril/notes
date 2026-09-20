# ARCH based distro Mac fan configuration - 

yay -S mbpfan

sudo systemctl enable --now mbpfan.service

sudo nvim /etc/mbpfan.conf

Update the exact same lines to protect the dual GPUs:
min_fan1_speed = 1200
max_fan1_speed = 2800
low_temp = 55
high_temp = 80

sudo systemctl restart mbpfan.service
