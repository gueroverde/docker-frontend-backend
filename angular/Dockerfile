FROM node:8-alpine

MAINTAINER Miguel Angel Sanchez Palafox <gueroverde@gmail.com>

RUN apk update \
  && apk add --update alpine-sdk \
  && npm install -g @angular/cli \
  && ng set --global packageManager=yarn \
  && apk del alpine-sdk \
  && rm -rf /tmp/* /var/cache/apk/* *.tar.gz ~/.npm \
  && npm cache clear \
  && sed -i -e "s/bin\/ash/bin\/sh/" /etc/passwd

#####################################
# Non-Root User:
#####################################



#RUN npm set progress=false && npm config set depth 0 && npm cache clean --force

## Storing node modules on a separate layer will prevent unnecessary npm installs at each build
##RUN npm i && mkdir /var/www/frontend/angular && cp -R ./node_modules /var/www/frontemd/angular




#USER root

#RUN npm install -g angular-cli; 



#WORKDIR /var/www/frontend/angular
#EXPOSE 4200


#ENTRYPOINT ["ng"]
#CMD ["--help"]

## Build the angular app in production mode and store the artifacts in dist folder
##RUN $(npm bin)/ng build --prod --build-optimizer
