Original from [Monogramm](https://github.com/Monogramm/docker-dolibarr)

## Dolibarr CRM 12.0.1
`amd64/php:7.2-apache`

Container Starup:
```
docker run -dit \
--name dolibarrcage \
--restart unless-stopped \
--link db01:mysql \
-v /home/user/dolibarr-12.0.1/htdocs:/var/www/html \
-v /home/user/dolibarr-12.0.1/scripts:/var/www/scripts \
-v /home/user/dolibarr-12.0.1/documents:/var/www/documents \
-e DOLI_AUTO_CONFIGURE='' \
-p 8088:80 \
akbartk/dolibarrcage:latest
```