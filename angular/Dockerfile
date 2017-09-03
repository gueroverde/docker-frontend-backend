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