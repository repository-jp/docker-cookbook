# The Recipe of PHPBrew 1.21.3 Docker Image

This directory contains Dockerfile of [PHPBrew](http://phpbrew.github.io/phpbrew/) for [Docker](https://www.docker.com/)'s automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

## Base Docker Image

[repositoryjp/centos:6.6](https://hub.docker.com/r/repositoryjp/centos/)

## Installation

[1] Install [Docker](https://www.docker.com/).

[2] Download automated build from public [Docker Hub Registry](https://hub.docker.com/): `docker pull repositoryjp/phpbrew-1.21.3`

## Usage

```
docker run -i -t -d -P repositoryjp/phpbrew-1.21.3
```

## How to create your PHP environment

If you want to use PHP, run below commands to create your PHP environment.

[1] Confirm installable versions by PHPBrew.

	phpbrew known

[2] Install PHP from PHPBrew.

	# Example:
	#
	# Install PHP 5.6.20
	#
	phpbrew install 5.6.20

[3] Switch an installed PHP as default.

	# Example:
	#
	# Switch PHP 5.6.20 as default
	#
	phpbrew switch 5.6.20

## License

See the file [LICENSE](../../../../../LICENSE).

## Author

[Shinya Kinoshita](http://www.shinyakinoshita.com) ( [REPOSITORY](http://www.repositories.jp) )
