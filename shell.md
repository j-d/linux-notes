## Links
Hard:     ln myFile.txt myLink.txt 
Simbolic: ln -s myFile.txt myLink.txt 
Mount:    sudo mount --bind folder target

## Deleting files and folders
rm -rf testing -prune

## Important file locations
/etc/passwd
/etc/krb5.conf
/etc/apt/apt.conf

## APT
apt-cache search ___
apt-get instal ___
apt-get update
apt-get remove -- purge
apt-get clean

## Samba
/etc/samba/smb.conf
/etc/init.d/samba start
chmod 777 /var/run/samba/winbindd...
/var/log/samba

## chmod
chown www-data:www-data ccr

## Live changes to textfile
tail -f /var/log

## Installed version of linux
cat /etc/*-release

## Kill 
killall -9 apache2

## Find a text in files
grep -r “_____” /home/

## Free space
df -h

## Other
mod_auth_kerb
file -b simbolic
