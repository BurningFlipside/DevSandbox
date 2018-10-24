NAME = burnerdev/php-appserver
VERSION = 7.1-apache

docker-build:
	docker build -t $(NAME):$(VERSION) --rm .
	docker tag $(NAME) $(NAME):$(VERSION)

docker-push:
	docker push $(NAME):$(VERSION)
