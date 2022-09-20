export DISPLAY

b build:
	$(info Construyendo contenedor..)
	@docker build -t firefox .
# permite que el usuario docker pueda interactuar con la sesión X
	@xhost + local:docker

r run:
	$(info Ejecutando firefox..)
	docker run --rm \
	-e DISPLAY=unix${DISPLAY} \
	-v /tmp/.X11-unix:/tmp/.X11-unix \
	--name firefox \
	firefox

#	docker run --rm -e DISPLAY=unix:$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix --name firefox
#	playniuniu/docker-gui-firefox
#	docker run -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=$DISPLAY -h $HOSTNAME -v $HOME/.Xauthority:/home/jelou/.Xauthority gui

.PHONY: b build r run
