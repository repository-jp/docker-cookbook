# The Recipe of Python Virtual Environment (pyenv-virtualenv) v20160315

This repository contains Dockerfile of [pyenv-virtualenv](https://github.com/yyuu/pyenv-virtualenv) for [Docker](https://www.docker.com/)'s automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

This image also contains "pyenv", a version management tool for Python.

## Base Docker Image

* [repositoryjp/centos:6.7](https://hub.docker.com/r/repositoryjp/centos/)

## pyenv Version

v20160422

## How to create and activate virtual environment for Python

If you want to use Python, run below commands to install Python that you want.

[1] Confirm installable versions by pyenv.

	pyenv install --list

[2] Install Python from pyenv.

	# Example:
	#
	# Install Python 2.7.11
	#
	pyenv install 2.7.11

[3] Create a virtual environment for Python using pyenv-virtualenv.

	# Example:
	#
	# Create a virtual environment named 'py27-latest' with Python 2.7.11
	#
	pyenv global 2.7.11
	pyenv virtualenv py27-latest

[4] Activate a virtual environment for Python using pyenv-virtualenv.

	# Example:
	#
	# Activate a virtual environment named 'py27-latest'.
	#
	pyenv activate py27-latest

## Installation

1. Install [Docker](https://www.docker.com/).

2. Download automated build from public [Docker Hub Registry](https://hub.docker.com/): `docker pull repositoryjp/pyenv-virtualenv-v20160422:cento-6.7`

## Usage

    docker run -i -t -d -P repositoryjp/pyenv-virtualenv-v20160422:cento-6.7

## License

See the file [LICENSE](../../../../../LICENSE).

## Author

[Shinya Kinoshita](http://www.shinyakinoshita.com) ( [REPOSITORY](http://www.repositories.jp) )
