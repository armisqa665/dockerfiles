FROM	ruby:3.4.7-alpine3.22
LABEL maintainer "Jessie Frazelle <jess@linux.com>"

RUN	apk add --no-cache \
	libcurl

RUN	set -x \
	&& apk add --no-cache --virtual .build-deps \
	build-base \
	&& gem install cloudapp --no-document \
	&& apk del .build-deps

ENTRYPOINT	["cloudapp"]
