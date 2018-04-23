# docker-apache2.4-test

## Usage

```bash
$ git clone git@github.com:ttskch/docker-apache2.4-test.git
$ cd docker-apache2.4-test
$ docker build docker -t test
$ docker run -it -v$(pwd):/var/www/html/test -p8888:80 test  
```

Then browse http://localhost:8888/{PATH}

| Url | Result |
| --- | --- |
| http://localhost:8888 | 403 |
| http://localhost:8888/public | 200 |
| http://localhost:8888/public/foo/bar | 200 |
| http://localhost:8888/index.php/public/foo/bar | 200 |
| http://localhost:8888/index.php/foo/bar | 403 |
| http://localhost:8888/index.php | 200 :sweat: |
