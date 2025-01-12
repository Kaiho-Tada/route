FROM nginx:1.27.3

RUN rm -f /etc/nginx/conf.d/*

COPY ./nginx.conf /etc/nginx/nginx.conf

CMD /usr/sbin/nginx -g 'daemon off;' -c /etc/nginx/nginx.conf
