FROM golang:alpine

# ############## author ##############
LABEL maintainer="fizzday <fizzday@yeah.net>" \
        Description="golang gorose alpine | latest"

# ############## env ##############
ENV TZ Asia/Shanghai
ENV GOROSE_VERSION master
ENV GO111MODULE on
ENV GOPRODIR /var/www/

# ############## golang dependency ###########
RUN apk add gcc
RUN apk add libc-dev
RUN apk add --no-cache git

# ############## work dir ###########
RUN mkdir -p $GOPRODIR
COPY demo/* $GOPRODIR

# ############## gorose init & run for once ###########
RUN cd $GOPRODIR && go mod tidy && go run main.go

WORKDIR $GOPRODIR