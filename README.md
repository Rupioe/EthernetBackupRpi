# EthernetBackupRpi
These scripts are not that portable, firstly because of the interfaces names, and for the set up of your backup disk. But the ip's are parsed at execution so it's not that bad.
When you will plug your computer to your hub or your station at home and boot on it, an automatic backup will be made (currently set to every 24 hours).
Your remote device with the connected drive needs to be pluged to the ethernet and powered on.

# Requirements
ifplugd
rsync
opensshd server on the remote computer
opensshd client on the machine to backup
generating rsa keys for the ssh connection


# Steps
Install the ifplugd directory content to /etc/ifplugd/
systemctl enable ifplugd@enp0s13f0u1u2u1.service && systemctl start ifplugd@enp0s13f0u1u2u1.service
replace enp0s13f0u1u2u1 with your ethernet interface name
