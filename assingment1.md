Mounting the Hard Disk:

sudo mount -o ro /dev/sdb1 test

cd test

Questions:

Name of the Computer:
Command: cat etc/hostname

OS Version:
Command: cat etc/os-release

Users:
Command: cat etc/passwd

Users with Sudo Permissions:
Command: cat etc/sudoers

Commands Executed by Different Users:
Commands:

cat home/sam/.bash_history

cat home/demo1/.bash_history

cat home/uadmin/.bash_history

Which User Installed Which Applications?:
Command: cat var/log/apt/history.log

SSH Logs and Source IP:
Command: cat var/log/syslog | grep ssh

Previous IPs Assigned to the Computer:
Command: cat var/log/syslog | grep ens33

Last Login:
Commands:

cd var/log

cat auth.log | grep login

Failed Login Attempts:
Commands:

cd var/log

faillog -a

Password-less SSH Allowed?:
Commands:

cd home/uadmin/.ssh

cat authorized_keys

