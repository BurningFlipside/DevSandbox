NAME = burnerdev/mysql
VERSION = 5.7

docker-build:
	docker build -t $(NAME):$(VERSION) --rm .
	docker tag $(NAME) $(NAME):$(VERSION)

docker-push:
	docker push $(NAME):$(VERSION)
