# Links
Hard:     ln myFile.txt myLink.txt 
Simbolic: ln -s myFile.txt myLink.txt 
Mount:    sudo mount --bind folder target

# Deleting files and folders
rm -rf testing -prune

# Important file locations
/etc/passwd
/etc/php5/apache2/php.ini
/etc/php5/cli/php.ini
/etc/apache2
/var/log/apache
/etc/krb5.conf
/etc/apache2/conf.d
/etc/apt/apt.conf
/usr/lib/apache2/modules
/etc/apache2/mods-enabled/....


# Apache
apache2ctl graceful
apache2ctl restart

# APT
apt-cache search ___
apt-get instal ___
apt-get update
apt-get remove -- purge
apt-get clean

# Samba
/etc/samba/smb.conf
/etc/init.d/samba start
chmod 777 /var/run/samba/winbindd...
/var/log/samba

# Chmod
chown www-data:www-data ccr

# Live changes to textfile
tail -f /var/log

# Installed version of linux
cat /etc/*-release

# Kill 
killall -9 apache2

# Find a text in files
grep -r “_____” /home/

# Free space
df -h

# Other
mod_auth_kerb
file -b simbolic
