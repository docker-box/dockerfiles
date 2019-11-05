FROM golang:alpine

# ############## author ##############
LABEL maintainer="fizzday <fizzday@yeah.net>" \
        Description="golang add dependency(gcc,libc-dev) with golang:alpine | latest"

# ############## env ##############
ENV TZ Asia/Shanghai
ENV PROXY https://goproxy.cn
ENV GO111MODULE on
ENV GOPRODIR /var/www

# ############## proxy ##############
RUN export GOPROXY=$PROXY

# ############## golang dependency ###########
RUN apk add gcc
RUN apk add libc-dev
RUN apk add --no-cache git

# ############## work dir ###########
RUN mkdir -p $GOPRODIR

WORKDIR $GOPRODIR