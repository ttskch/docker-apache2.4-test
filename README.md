# docker-apache2.4-test

## Usage

```bash
$ git clone git@github.com:ttskch/docker-apache2.4-test.git
$ cd docker-apache2.4-test
$ docker build docker -t test
$ docker run -it -v$(pwd):/var/www/html/test -p8888:80 test  
```
