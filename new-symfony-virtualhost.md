Create the script

```
cd

tee ./new-symfony-virtualhost << EOS
echo "Please enter the project name"
echo "e.g. testproject"
read PROJECT_NAME

echo 127.0.0.1 \${PROJECT_NAME}.local | sudo tee -a /etc/hosts

sudo tee /etc/apache2/sites-available/${PROJECT_NAME} << EOF
  <VirtualHost *:80>
    DocumentRoot "/var/www/${PROJECT_NAME}/web"
    DirectoryIndex app.php
    ServerName \${PROJECT_NAME}.local
    <Directory "/var/www/${PROJECT_NAME}/web">
      AllowOverride All
      Allow from All
    </Directory>
  </VirtualHost>
EOF

sudo a2ensite \${PROJECT_NAME}
sudo service apache2 reload
EOS
chmod u+x ./new-symfony-virtualhost
```

Run it and it will prompt you for the project name
```
sudo ./new-symfony-virtualhost
```

Go to the new folder
```
cd /var/www
```
