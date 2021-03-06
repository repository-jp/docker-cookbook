# The Recipe of MySQL 5.6.29 Docker Image

This directory contains Dockerfile of [MySQL](https://www.mysql.com/) 5.6.29 for [Docker](https://www.docker.com/)'s automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

## Base Docker Image

[repositoryjp/centos:6.7](https://hub.docker.com/r/repositoryjp/centos/)

## Installation

[1] Install [Docker](https://www.docker.com/).

[2] Download automated build from public [Docker Hub Registry](https://hub.docker.com/): `docker pull repositoryjp/mysql-5.6.29:centos-6.7`

## Usage

```
docker run -d -p (host's port for mysql):3306 -v (host's path for mysql's data directory):/var/lib/mysql repositoryjp/mysql-5.6.29:centos-6.7
```

[options]

* Port number for mysql (required) : -p (host's port for mysql):3306
* Data directory path (optional) : -v (host's path for mysql's data directory):/var/lib/mysql

## License

See the file [LICENSE](../../../../../../LICENSE).

## Author

[Shinya Kinoshita](http://www.shinyakinoshita.com) ( [REPOSITORY](http://www.repositories.jp) )
