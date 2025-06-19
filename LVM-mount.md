## TO mount LVM

sudo apt-get install lvm2

sudo lvs
sudo vgscan
sudo vgchange -ay
sudo vgdisplay

sudo mkdir /mnt/forensic/home
sudo mkdir /mnt/forensic/root

sudo mount -o ro /dev/rl/home /mnt/forensic/home
sudo mount -o ro /dev/rl/home /mnt/forensic/root