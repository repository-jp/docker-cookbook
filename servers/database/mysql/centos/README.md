# The Recipe of MySQL Docker Image

This directory contains Dockerfile of [MySQL](https://www.mysql.com/) for [Docker](https://www.docker.com/)'s automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

## Base Docker Image

[repositoryjp/centos:6.6](https://hub.docker.com/r/repositoryjp/centos/)


## MySQL Version

5.6.29

## Installation

[1] Install [Docker](https://www.docker.com/).

[2] Download automated build from public [Docker Hub Registry](https://hub.docker.com/): `docker pull repositoryjp/mysql`

## Usage

```
docker run -d -p (host's port for mysql):3306 -v (host's path for mysql's data directory):/var/lib/mysql repositoryjp/mysql
```

[options]

* Port number for mysql (required) : -p (host's port for mysql):3306
* Data directory path (optional) : -v (host's path for mysql's data directory):/var/lib/mysql


## License

See the file [LICENSE](../../../../LICENSE).

## Author

[Shinya Kinoshita](http://www.shinyakinoshita.com) ( [REPOSITORY](http://www.repositories.jp) )

