FROM node:7.10

MAINTAINER Miguel Angel Sanchez Palafox <gueroverde@gmail.com>

RUN mkdir -p /var/www/frontend/angular

WORKDIR /var/www/frontend/angular

# Just for dev
RUN npm install @angular/cli -g
#RUN npm install mocha -g
#RUN npm install knex -g

# Opting for COPY over ADD as there is no need of auto extracting any compressed file

#RUN npm install

#CMD npm start

EXPOSE 4200
CMD [ "node" ]


#RUN apk update \
 # && apk add --update alpine-sdk \
 # && npm install -g @angular/cli \
 ## && ng set --global packageManager=yarn \
 # && apk del alpine-sdk \
 # && rm -rf /tmp/* /var/cache/apk/* *.tar.gz ~/.npm \
 # && npm cache clear \
 # && sed -i -e "s/bin\/ash/bin\/sh/" /etc/passwd

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
