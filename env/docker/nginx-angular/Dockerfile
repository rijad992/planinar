FROM nginx:alpine

COPY nginx.conf /etc/nginx/
COPY sites/angular.conf /etc/nginx/conf.d/
RUN rm -f /etc/nginx/conf.d/default.conf

RUN set -x ; \
  addgroup -g 82 -S www-data ; \
  adduser -u 1000 -D -S -G www-data www-data && exit 0 ; exit 1

EXPOSE 8080 443