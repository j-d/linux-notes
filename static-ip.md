```
sudo nano /etc/network/interfaces
```
Find and remove:
```
iface eth0 inet dhcp
```
Add:
```
iface eth0 inet static
address 192.168.110.200
netmask 255.255.255.0
network 192.168.110.0
broadcast 192.168.110.255
gateway 192.168.110.2
```
Save and close the file

Now we’ll need to add in the DNS settings by editing the resolv.conf file:

```
sudo nano /etc/resolv.conf
```
Add:
```
nameserver 10.31.242.164
nameserver 10.1.1.7
nameserver 10.1.1.3
search arkonline.local
```

You need to also remove the dhcp client for this to stick (thanks to Peter for noticing). You might need to remove dhcp-client3 instead.

```
sudo apt-get remove dhcp-client
```

Restart the network:
```
sudo restart networking
```
