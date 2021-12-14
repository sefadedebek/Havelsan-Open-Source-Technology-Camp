# Apache sunucusu kurma

Apache paketini kurma;

```
sudo apt-get install apache2
```


Apachi servisi kurulumu komut ile tamamlanıyor ama port çakışmasından dolayı sunucu başlatılamıyor. "Failed to start The Apache HTTP Server" hatası alıyoruz;
Bu Hatayı Çömek için sunucunun kurulu olduğu portu değiştiriyoruz.;



```
sudo nano /etc/apache2/ports.conf
```

```
# If you just change the port or add more ports here, you will likely also
# have to change the VirtualHost statement in
# /etc/apache2/sites-enabled/000-default.conf

Listen 90

<IfModule ssl_module>
        Listen 443
</IfModule>

<IfModule mod_gnutls.c>
        Listen 443
</IfModule>

# vim: syntax=apache ts=4 sw=4 sts=4 sr noet
```


Apache sunucusunu hatasız bir şekilde başlatıyoruz.;


```
sudo /etc/init.d/apache2 start
```


Log dosyalarını ayarlamak ve arşivlemek için Logrotate paketini kuruyoruz.;



```
sudo apt-get install logrotate -y
```


Apache pakeitnin loglarının ayarlanması için Logrotate ile dosyasının üzerinde değişiklikler yapıyoruz.;

```
sudo nano /etc/logrotate.d/apache2
```


```
/var/log/apache2/*.log {
        daily
        missingok
        rotate 14
        compress
        delaycompress
        notifempty
        create 640 root adm
        size 20
        sharedscripts
        postrotate
                if invoke-rc.d apache2 status > /dev/null 2>&1; then \
                    invoke-rc.d apache2 reload > /dev/null 2>&1; \
                fi;
        endscript
        prerotate
                if [ -d /etc/logrotate.d/httpd-prerotate ]; then \
                        run-parts /etc/logrotate.d/httpd-prerotate; \
                fi; \
        endscript
}
```


Daha sonra kaydedip tekrar çalıştırıyoruz.;

