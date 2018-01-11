DOCKERFILE = Dockerfile
NAME = cdev
HUB_USERNAME = sdll
REPO = $(HUB_USERNAME)/$(NAME)
build:
	sudo docker build -f $(DOCKERFILE) -t $(NAME) .
stash:
	sudo docker login
	sudo docker tag $(NAME) $(REPO)
	sudo docker push $(REPO)
