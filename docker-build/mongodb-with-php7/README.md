
Getting started for Docker Engine CE (Free Version)
---------------------------------------------------

```
sudo mkdir -p /build && cd /build

sudo apt-get install git -y && sudo git clone https://github.com/drivesoft-technology/docker-awesome.git

cd /build/docker-awesome
```


Install Docker Engine CE v17.12.0 (Free Version)
---------------------------------------------------

```
bash /build/docker-awesome/docker-install/install-docker-engine-on-ubuntu16.sh
```


Install Docker Compose v1.19.0
---------------------------------------------------

```
bash /build/docker-awesome/docker-install/install-docker-compose-on-ubuntu16.sh
```


Build MongoDB PHP Mobule.
---------------------------------------------------

```
docker build -t build/php7mongo:7.2.2 .
```


```
docker run -it --name docker-php7mongo -d build/php7mongo:7.2.2
docker cp docker-php7mongo:/usr/local/etc/php/conf.d/mongodb.ini ./php7-ini/mongodb.ini
docker cp docker-php7mongo:/usr/local/lib/php/extensions/no-debug-non-zts-20170718/mongodb.so ./php7-ext/mongodb.so
```


```
docker stop docker-php7mongo && docker rm docker-php7mongo
```