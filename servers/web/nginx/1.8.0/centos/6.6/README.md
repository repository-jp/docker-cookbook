# The Recipe of Nginx 1.8.0 Docker Image

This directory contains Dockerfile of [Nginx](http://nginx.org/en/) 1.8.0 for [Docker](https://www.docker.com/)'s automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

## Base Docker Image

[repositoryjp/centos:6.6](https://hub.docker.com/r/repositoryjp/centos/)

## Installation

[1] Install [Docker](https://www.docker.com/).

[2] Download automated build from public [Docker Hub Registry](https://hub.docker.com/): `docker pull repositoryjp/nginx-1.8.0:centos-6.6`

## Usage

```
docker run -d -p (host's port for http):80 -p (host's port for https):443 -v (host's path for nginx configuration):/etc/nginx/conf.d/ -v (host's path for document root):/usr/share/nginx/ -v (host's path for logfile):/var/log/nginx repositoryjp/nginx-1.8.0:centos-6.6
```

[options]

* Port number for http (required) : -p (host's port for http):80
* Port number for https (optional) : -p (host's port for https):443
* Nginx configuration path (optional) : -v (host's path for nginx configuration):/etc/nginx/conf.d/
* Document root path (optional) : -v (host's path for document root):/usr/share/nginx/
* Logfile path (optional) : -v (host's path for logfile):/var/log/nginx repositoryjp/nginx


## License

See the file [LICENSE](../../../../../LICENSE).

## Author

[Shinya Kinoshita](http://www.shinyakinoshita.com) ( [REPOSITORY](http://www.repositories.jp) )
