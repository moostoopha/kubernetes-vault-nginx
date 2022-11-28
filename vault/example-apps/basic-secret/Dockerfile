FROM nginx:alpine
RUN apk update
RUN apk add apache2-utils
WORKDIR /etc/apache2/
## Remove default nginx index page

# copy the package.json to install dependencies
COPY ./default.conf /etc/nginx/conf.d/default.conf
COPY ./htpasswd /etc/nginx/.htpasswd

# Expose port
EXPOSE 8080

ENTRYPOINT ["nginx", "-g", "daemon off;"]
