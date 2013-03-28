Enter sudo mode
```
sudo ls
```

```
echo 127.0.0.1 $2.local | sudo tee -a /etc/hosts

sudo tee /etc/apache2/sites-available/$2 << EOF
  <VirtualHost *:80>
    DocumentRoot "/var/www/$2/web"
    DirectoryIndex app.php
    ServerName $2.local
    <Directory "/var/www/$2/web">
      AllowOverride All
      Allow from All
    </Directory>
  </VirtualHost>
EOF

sudo a2ensite application
sudo service apache2 reload

cd /var/www
```
