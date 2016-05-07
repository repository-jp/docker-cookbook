# The Recipe of virtPHP 0.5.2 Docker Image

This directory contains Dockerfile of [virtPHP](http://virtphp.org/) for [Docker](https://www.docker.com/)'s automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

This image also contains "PHPBrew", a version management tool for PHP.

## Base Docker Image

[repositoryjp/centos:6.6](https://hub.docker.com/r/repositoryjp/centos/)

## PHPBrew Version

1.21.3

## Installation

[1] Install [Docker](https://www.docker.com/).

[2] Download automated build from public [Docker Hub Registry](https://hub.docker.com/): `docker pull repositoryjp/virtphp`

## Usage

```
docker run -i -t -d -P repositoryjp/virtphp
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

[3] Create a virtual environment for PHP using virtPHP.

	# Example:
	#
	# Create a virtual environment named 'phpenv' with PHP 5.6.20.
	#
	virtphp create --php-bin-dir=$HOME/.phpbrew/php/php-5.6.20/bin phpenv

## How to activate your PHP environment

If you want to activate your PHP environment, run below command.

	# Example:
	#
	# Activate a virtual environment named 'phpenv'.
	#
	source $HOME/.virtphp/envs/phpenv/bin/activate

## License

See the file [LICENSE](../../../../../LICENSE).

## Author

[Shinya Kinoshita](http://www.shinyakinoshita.com) ( [REPOSITORY](http://www.repositories.jp) )
