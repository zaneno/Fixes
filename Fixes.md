## Resolution stuck at 640x480

/usr/bin/python3 /usr/bin/software-properties-gtk --open-tab 4

# switch to the Nvidia proprietary driver
# reboot


## QEMU/KVM connection...
# ugh

# check that you are still in the libvirt group
groups

# check that libvirt is working at system adn session levels
virsh -c qemu:///system
virsh -c qemu:///session

# WHAT WORKED FOR ME
sudo systemctl stop libvirtd.service
sudo systemctl start libvirtd.service
