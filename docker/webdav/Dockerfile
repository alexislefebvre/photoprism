FROM golang:1

LABEL maintainer="Michael Mayer <hello@photoprism.org>"

# Set up project directory
WORKDIR "/webdav"

RUN go get github.com/hacdias/webdav

# Expose HTTP port
EXPOSE 80

COPY /docker/webdav/config.yml /webdav/config.yml
COPY /docker/webdav/files /webdav/files

CMD webdav -c /webdav/config.yml
