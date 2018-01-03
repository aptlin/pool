# Run Libreoffice in a container

# docker run -d \
#	-v /etc/localtime:/etc/localtime:ro \
#	-v /tmp/.X11-unix:/tmp/.X11-unix \
#	-e DISPLAY=$DISPLAY \
#	-v $HOME/werke:/root/werke\
#	-e GDK_SCALE \
#	-e GDK_DPI_SCALE \
#	--name libreoffice \
#	sdll/libreoffice
#

FROM alpine:latest
LABEL maintainer "Sasha Illarionov <sasha.delly@gmail.com>"

RUN apk --no-cache add \
  --repository https://dl-3.alpinelinux.org/alpine/edge/testing \
  libreoffice \
  ttf-dejavu

ENTRYPOINT [ "libreoffice" ]
