# The Recipe of Python Version Management (pyenv) v20160422

This repository contains Dockerfile of [pyenv](https://github.com/yyuu/pyenv) for [Docker](https://www.docker.com/)'s automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

## Base Docker Image

* [repositoryjp/centos:6.7](https://hub.docker.com/r/repositoryjp/centos/)

## How to install Python

If you want to use Python, run below commands to install Python that you want.

[1] Confirm installable versions by pyenv.

	pyenv install --list

[2] Install Python from pyenv.

	# Example:
	#
	# Install Python 2.7.11
	#
	pyenv install 2.7.11

## Installation

1. Install [Docker](https://www.docker.com/).

2. Download automated build from public [Docker Hub Registry](https://hub.docker.com/): `docker pull repositoryjp/pyenv-v20160422:cento-6.7`

## Usage

    docker run -i -t -d -P repositoryjp/pyenv-v20160422:cento-6.7

## License

See the file [LICENSE](../../../../../LICENSE).

## Author

[Shinya Kinoshita](http://www.shinyakinoshita.com) ( [REPOSITORY](http://www.repositories.jp) )
