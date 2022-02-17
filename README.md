17 Feb 2022: minor layout tweaks to make it centered

# subnets
Visual subnet calculator as seen at http://www.davidc.net/sites/default/subnets/subnets.html

Run with docker

```
cd <project folder>
docker build . -t subnets
docker run -d -p 5001:80 --name subnets subnets
```

or just have a look inside the Dockerfile and make some changes to pop the contents in a subdirectory of your webserver. Docker not required. 

```
FROM php:5.6-apache

COPY index.php gennum.php subnets.html /var/www/html/
COPY img/* /var/www/html/img/
```
