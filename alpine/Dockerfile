FROM python:3.6-alpine

RUN 	echo "http://dl-4.alpinelinux.org/alpine/edge/testing/" >> /etc/apk/repositories \
        && echo "http://dl-5.alpinelinux.org/alpine/edge/testing/" >> /etc/apk/repositories \
	&& apk add --no-cache --update --virtual .build-deps curl gcc g++ geos \ 
	&& ln -s /usr/include/locale.h /usr/include/xlocale.h \
	&& pip install partridge gtfstk numpy pandas boto3 tqdm \
	&& apk del .build-deps

CMD python3
