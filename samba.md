## Mount Samba Share permanently

https://help.ubuntu.com/community/MountWindowsSharesPermanently

```
sudo apt-get install smbfs
```

```
cd
mkdir .smbcredentials
cd .smbcredentials
sudo tee .truecrypt1 << EOF
username=domainOrWorkgroup/user
password=password
EOF

sudo chown root .truecrypt1
sudo chmod 600 .truecrypt1

cd

sudo mkdir /mnt/truecrypt1
echo //computer/share /mnt/truecrypt1 smbfs credentials=/home/jose/.smbcredentials/.truecrypt1,uid=1000,gid=1000 | sudo tee -a /etc/fstab
sudo mount -a

# The 1000 is from /etc/passwd
```
