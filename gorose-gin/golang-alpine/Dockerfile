FROM go-depend

# ############## author ##############
LABEL maintainer="fizzday <fizzday@yeah.net>" \
        Description="golang gorose-gin alpine | latest"

# ############## env ##############
ENV TZ Asia/Shanghai
ENV GOROSE_GIN_VERSION master
ENV GO111MODULE on

# ############## proxy ##############
RUN export GOPROXY=https://goproxy.cn

# ############## gorose-gin init & run for once ###########
ENV GOPRODIR /go/src/gopro/
COPY demo/* $GOPRODIR
RUN cd $GOPRODIR && go mod tidy && go mod download

WORKDIR $GOPRODIR