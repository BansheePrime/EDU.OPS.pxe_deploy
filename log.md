apt update && apt upgrade -y

apt install sudo
adduser gidra sudo

sudo apt install --no-install-recommends qemu-system libvirt-clients libvirt-daemon-system
adduser gidra libvirt

sudo install vagrant vagrant-libvirt
sudo install ansible

