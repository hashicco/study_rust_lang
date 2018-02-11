FROM frolvlad/alpine-rust:latest

ARG APP_ROOT=/var/app
ARG FILES=.

ENV BASE_PACKAGES="build-base bash openssh-client git" \
    DEV_PACKAGES="" \
    ETC_PACKAGES="tzdata"

RUN mkdir -p ${APP_ROOT}
WORKDIR $APP_ROOT
EXPOSE 3000

RUN set -ex \
    && apk update \
    && apk upgrade \
    && apk add --update --no-cache\
        $BASE_PACKAGES \
        $DEV_PACKAGES \
        $ETC_PACKAGES \
    && rm -f /etc/localtime \
    && ln -s /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
    && echo

ENTRYPOINT ["tail", "-f", "/dev/null"]

