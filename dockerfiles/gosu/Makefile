NAME = burnerdev/gosu
VERSION = 1.11

docker-build:
	docker build -t $(NAME) .
	docker tag $(NAME) $(NAME):$(VERSION)

docker-push:
	docker push $(NAME):$(VERSION)
