## creating a DD img

### To check the disk
lsblk

### To create a partion 
fdisk  /dev/sdb

n
p
defualt
enter
enter 
w -> to save
p -> to print 

### To format
--> create a mnt of frensic
mkfs.ext4 /dev/sdb1
mount 0t auto /dev/sdb1 /mnt/forensic
cd /mnt/forensic
---> create files here

--> umount /dev/forensic

### Create DD image

dd if=/dev/sdb of=case.img bs=512



--> can verify using md5sum or SHA256 


## Different mounting patterns
for e.g
sudo mount /dev/sdb  /mnt/ditiss
sudo mount -t auto /dev/sdb  /mnt/ditiss
sudo mount -o ro /dev/sdb /mnt/ditiss


sudo munt -o loop,oofset=16384, /dev/sdb /mnt/forensic