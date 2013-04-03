##Integrate PHPunit code coverage on PHPStorm)

```
sudo tee -a /etc/php5/apache2/php.ini << EOF
xdebug.remote_enable=1
xdebug.remote_host=localhost
xdebug.remote_port=9000
xdebug.profiler_enable=1
EOF
sudo apache2ctl restart
```

Click on configurations > Edit configurations > + > PHPUnit
Name: xxx
Defined in the configuration file

Configure PHP interpreter
