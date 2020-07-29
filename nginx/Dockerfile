FROM nginx:1.15.12-alpine

COPY nginx.conf /etc/nginx/

RUN apk update \
    && apk upgrade \
    && apk add --no-cache openssl \
    && apk add --no-cache bash \
    && adduser -D -H -u 1000 -s /bin/bash www-data

# Remove the default conf
RUN rm /etc/nginx/conf.d/default.conf

EXPOSE 80 443

CMD ["nginx"]
