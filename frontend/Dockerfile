FROM nginx
RUN rm -rf /usr/share/nginx/html/index.html
RUN rm -rf /ect/nginx/nginx.conf
RUN rm -rf /etc/nginx/conf.d/default.conf
ADD nginx.conf /ect/nginx/nginx.conf
ADD static/ /user/share/nginx/html/
