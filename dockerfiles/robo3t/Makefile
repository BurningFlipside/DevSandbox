NAME = burnerdev/robo3t
VERSION = latest

docker-build:
	docker build -t $(NAME):$(VERSION) --rm .
	docker tag $(NAME) $(NAME):$(VERSION)

docker-push:
	docker push $(NAME):$(VERSION)
