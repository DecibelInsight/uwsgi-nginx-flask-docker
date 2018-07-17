#
# Makefile
#

VERSION=0.1
NAME=gbroccolo/uwsgi-nginx-flask:python2.7-alpine3.7-pandas-scipy-scikitlearn

default: build

tag:
	docker tag $(NAME) $(NAME):$(VERSION)
	docker tag $(NAME) $(NAME):latest
	git tag $(VERSION)

push:
	git push --tags
	docker push $(NAME):$(VERSION)
	docker push $(NAME):latest

build:
	docker build -t $(NAME) .

all:
	@echo "Makefile needs your attention"

# vim:ft=make
#
