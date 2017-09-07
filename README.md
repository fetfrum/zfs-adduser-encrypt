# ZFS-adduser-encrypt
### Installation
`git clone https://github.com/fetfrum/zfs-adduser-encrypt
cd zfs-adduser-encrypt
sudo cp adduser /usr/local/sbin/
`

This file overrides the system adduser, but doesn't overwrite it
### Usage
Normal mod:
'adduser <new-username>' 

Encrypted mod:
'adduser --encrypt-home <new-username>'

In encrypted mode, if this scrypt detected zfs-filesystem on mountpoint /home then create new dataset at <pool>/home/<new-username> with mountpoint /home/.ecryptedfs/<new-username>. 
