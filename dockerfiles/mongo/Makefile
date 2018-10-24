NAME = burnerdev/mongo
VERSION = 3.4

docker-build:
	docker build -t $(NAME):$(VERSION) --rm .
	docker tag $(NAME) $(NAME):$(VERSION)

docker-push:
	docker push $(NAME):$(VERSION)
