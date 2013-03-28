## Mount SSH Share permanently - doesn’t work as desired

http://www.howtogeek.com/howto/ubuntu/how-to-mount-a-remote-folder-using-ssh-on-ubuntu/

```
sudo apt-get install sshfs
sudo modprobe fuse
sudo adduser USER fuse
sudo chown root:fuse /dev/fuse
```

LOGOFF / LOGON

```
sudo sshfs USER@COMPUTER_NAME:/media/PATH_TO_FOLDER /var/www/PATH

sshfs#USER@COMPUTER_NAME:/media/PATH_TO_FOLDER    /var/www/PATH   fuse    user,transform_symlinks 0 0
```

doesn’t work
