apt update && apt upgrade -y

apt install sudo
adduser gidra sudo

sudo apt install vim

sudo apt install --no-install-recommends qemu-system libvirt-clients libvirt-daemon-system
adduser gidra libvirt

ssh-keygen -b 2048 -t rsa -f ~/.ssh/debi-vtt
ssh-copy-id

sudo install vagrant vagrant-libvirt
sudo install ansible

