FROM nginx:latest

# Adding custom index.html 
ADD public.html /usr/share/nginx/html/
RUN rm /usr/share/nginx/html/index.html

RUN rm /etc/nginx/conf.d/default.conf
COPY default.conf /etc/nginx/conf.d/default.conf

# Adding read permissions to custom index.html
RUN chmod +r /usr/share/nginx/html/public.html

# 'nginx -g daemon off" will run as default command when any container is run that uses the image that was built using this Dockerfile"
CMD ["nginx", "-g", "daemon off;"]