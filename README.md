# docker-wordpress

## Images
based on official:
- nginx:mainline-alpine
- wordpress:4.6-fpm
- mariadb:10.1

like docker-lemp, nginx got his dockerfile to be up to date  
wordpress got as well his own makefile, running on alpine linux  

## Config
remove sample to all .env file and config them to your need  

notice the difference in domainewhateveryouwant.conf compared to docker-lemp:  

```
location / {
	root	/var/www/html/wordpress01;
}
location ~ \.php$ {
	root	/var/www/html;
}
```

i can by exemple, make several wordpress instance with the same nginx container

