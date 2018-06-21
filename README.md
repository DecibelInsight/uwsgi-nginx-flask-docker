uwsgi-nginx-flask-docker
========================

`Pandas` and `SciPy` Python libraries needs `glibc` headers in order to be installed
through `pip`. In latest Alpine distributions, the needed `glibc` header has been renamed.
Furthermore, the latest `NumPy` release (1.14.4) breake the installation of `Pandas`.
At the moment, the PyPI community didn't fixed this stuff, so this is a repo to build
a Docker image based on Alpine containing the workaround for the installation of
`NumPy`/`Pandas`:

* proper link to the needed `glibc` header
* preventive build of `Pandas` dependencies in order to avoid the latest `NumPy` version

As parent image, we considered `tiangolo/uwsgi-nginx-flask:python2.7-alpine3.7`
(https://github.com/tiangolo/uwsgi-nginx-flask-docker/tree/master/python2.7-alpine3.7), so
the resulting image will host a Python 2.7 Flask application based on uWSGI and Nginx with
scientific libraries installed.
