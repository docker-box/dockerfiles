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

# ############## gorose init & run for once ###########
RUN cd /go/src/gopro && go mod tidy && go mod download

WORKDIR /go/src/gopro