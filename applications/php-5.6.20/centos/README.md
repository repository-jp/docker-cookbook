# The Recipe of PHP 5.6.20 Docker Image

This directory contains Dockerfile of [PHP](http://php.net/) 5.6.20 for [Docker](https://www.docker.com/)'s automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

## Base Docker Image

[repositoryjp/virtphp](https://hub.docker.com/r/repositoryjp/virtphp/)

## PHP Version

5.6.20

## Installation

[1] Install [Docker](https://www.docker.com/).

[2] Download automated build from public [Docker Hub Registry](https://hub.docker.com/): `docker pull repositoryjp/php-5.6.20`

## Usage

```
docker run -i -t -d -P repositoryjp/php-5.6.20
```

## License

See the file [LICENSE](../../../LICENSE).

## Author

[Shinya Kinoshita](http://www.shinyakinoshita.com) ( [REPOSITORY](http://www.repositories.jp) )
